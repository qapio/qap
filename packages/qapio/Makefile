VERSION=1.0.149
NAME=qapio
DIST=../../dist

release:
	gh release create ${NAME} --notes ${NAME}

upload:
	gh release upload ${NAME} ${DIST}/${NAME}/${NAME}@${VERSION}/*

package:
	/home/linuxbrew/.linuxbrew/bin/pkl project package -e VERSION=${VERSION} -w src --output-path ../${DIST}/${NAME}/${NAME}@${VERSION}

resolve:
	/home/linuxbrew/.linuxbrew/bin/pkl project resolve -w . -e VERSION=${VERSION} src


deploy: resolve package upload
