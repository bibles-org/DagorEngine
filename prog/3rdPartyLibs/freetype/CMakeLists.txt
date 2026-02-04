set(FREETYPE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/freetype-2.8)

add_library(freetype STATIC)

target_include_directories(freetype
        PUBLIC
        ${FREETYPE_DIR}/include
        ${FREETYPE_DIR}/src
)

target_compile_definitions(freetype
        PRIVATE
        FT2_BUILD_LIBRARY
)

target_sources(freetype PRIVATE
        ${FREETYPE_DIR}/src/autofit/afangles.c
        ${FREETYPE_DIR}/src/autofit/afblue.c
        ${FREETYPE_DIR}/src/autofit/afcjk.c
        ${FREETYPE_DIR}/src/autofit/afdummy.c
        ${FREETYPE_DIR}/src/autofit/afglobal.c
        ${FREETYPE_DIR}/src/autofit/afhints.c
        ${FREETYPE_DIR}/src/autofit/afindic.c
        ${FREETYPE_DIR}/src/autofit/aflatin.c
        ${FREETYPE_DIR}/src/autofit/afloader.c
        ${FREETYPE_DIR}/src/autofit/afmodule.c
        ${FREETYPE_DIR}/src/autofit/afpic.c
        ${FREETYPE_DIR}/src/autofit/afranges.c
        ${FREETYPE_DIR}/src/autofit/afshaper.c
        ${FREETYPE_DIR}/src/autofit/afwarp.c

        ${FREETYPE_DIR}/src/base/basepic.c
        ${FREETYPE_DIR}/src/base/ftadvanc.c
        ${FREETYPE_DIR}/src/base/ftcalc.c
        ${FREETYPE_DIR}/src/base/ftdbgmem.c
        ${FREETYPE_DIR}/src/base/ftgloadr.c
        ${FREETYPE_DIR}/src/base/fthash.c
        ${FREETYPE_DIR}/src/base/ftobjs.c
        ${FREETYPE_DIR}/src/base/ftoutln.c
        ${FREETYPE_DIR}/src/base/ftpic.c
        ${FREETYPE_DIR}/src/base/ftrfork.c
        ${FREETYPE_DIR}/src/base/ftsnames.c
        ${FREETYPE_DIR}/src/base/ftstream.c
        ${FREETYPE_DIR}/src/base/fttrigon.c
        ${FREETYPE_DIR}/src/base/ftutil.c
        ${FREETYPE_DIR}/src/base/ftapi.c
        ${FREETYPE_DIR}/src/base/ftbbox.c
        ${FREETYPE_DIR}/src/base/ftbdf.c
        ${FREETYPE_DIR}/src/base/ftbitmap.c
        ${FREETYPE_DIR}/src/base/ftcid.c
        ${FREETYPE_DIR}/src/base/ftdebug.c
        ${FREETYPE_DIR}/src/base/ftfntfmt.c
        ${FREETYPE_DIR}/src/base/ftfstype.c
        ${FREETYPE_DIR}/src/base/ftgasp.c
        ${FREETYPE_DIR}/src/base/ftglyph.c
        ${FREETYPE_DIR}/src/base/ftgxval.c
        ${FREETYPE_DIR}/src/base/ftinit.c
        ${FREETYPE_DIR}/src/base/ftlcdfil.c
        ${FREETYPE_DIR}/src/base/ftmm.c
        ${FREETYPE_DIR}/src/base/ftotval.c
        ${FREETYPE_DIR}/src/base/ftpatent.c
        ${FREETYPE_DIR}/src/base/ftpfr.c
        ${FREETYPE_DIR}/src/base/ftstroke.c
        ${FREETYPE_DIR}/src/base/ftsynth.c
        ${FREETYPE_DIR}/src/base/ftsystem.c
        ${FREETYPE_DIR}/src/base/fttype1.c
        ${FREETYPE_DIR}/src/base/ftwinfnt.c

        ${FREETYPE_DIR}/src/bdf/bdfdrivr.c
        ${FREETYPE_DIR}/src/bdf/bdflib.c

        ${FREETYPE_DIR}/src/cache/ftcbasic.c
        ${FREETYPE_DIR}/src/cache/ftccache.c
        ${FREETYPE_DIR}/src/cache/ftcglyph.c
        ${FREETYPE_DIR}/src/cache/ftcimage.c
        ${FREETYPE_DIR}/src/cache/ftcmanag.c
        ${FREETYPE_DIR}/src/cache/ftccmap.c
        ${FREETYPE_DIR}/src/cache/ftcmru.c
        ${FREETYPE_DIR}/src/cache/ftcsbits.c

        ${FREETYPE_DIR}/src/cff/cffcmap.c
        ${FREETYPE_DIR}/src/cff/cffdrivr.c
        ${FREETYPE_DIR}/src/cff/cffgload.c
        ${FREETYPE_DIR}/src/cff/cffload.c
        ${FREETYPE_DIR}/src/cff/cffobjs.c
        ${FREETYPE_DIR}/src/cff/cffparse.c
        ${FREETYPE_DIR}/src/cff/cffpic.c
        ${FREETYPE_DIR}/src/cff/cf2arrst.c
        ${FREETYPE_DIR}/src/cff/cf2blues.c
        ${FREETYPE_DIR}/src/cff/cf2error.c
        ${FREETYPE_DIR}/src/cff/cf2font.c
        ${FREETYPE_DIR}/src/cff/cf2ft.c
        ${FREETYPE_DIR}/src/cff/cf2hints.c
        ${FREETYPE_DIR}/src/cff/cf2intrp.c
        ${FREETYPE_DIR}/src/cff/cf2read.c
        ${FREETYPE_DIR}/src/cff/cf2stack.c

        ${FREETYPE_DIR}/src/raster/ftraster.c
        ${FREETYPE_DIR}/src/raster/ftrend1.c
        ${FREETYPE_DIR}/src/raster/rastpic.c

        ${FREETYPE_DIR}/src/sfnt/pngshim.c
        ${FREETYPE_DIR}/src/sfnt/sfdriver.c
        ${FREETYPE_DIR}/src/sfnt/sfntpic.c
        ${FREETYPE_DIR}/src/sfnt/sfobjs.c
        ${FREETYPE_DIR}/src/sfnt/ttbdf.c
        ${FREETYPE_DIR}/src/sfnt/ttcmap.c
        ${FREETYPE_DIR}/src/sfnt/ttkern.c
        ${FREETYPE_DIR}/src/sfnt/ttload.c
        ${FREETYPE_DIR}/src/sfnt/ttmtx.c
        ${FREETYPE_DIR}/src/sfnt/ttpost.c
        ${FREETYPE_DIR}/src/sfnt/ttsbit.c

        ${FREETYPE_DIR}/src/smooth/ftgrays.c
        ${FREETYPE_DIR}/src/smooth/ftsmooth.c
        ${FREETYPE_DIR}/src/smooth/ftspic.c

        ${FREETYPE_DIR}/src/truetype/ttdriver.c
        ${FREETYPE_DIR}/src/truetype/ttgload.c
        ${FREETYPE_DIR}/src/truetype/ttgxvar.c
        ${FREETYPE_DIR}/src/truetype/ttinterp.c
        ${FREETYPE_DIR}/src/truetype/ttobjs.c
        ${FREETYPE_DIR}/src/truetype/ttpic.c
        ${FREETYPE_DIR}/src/truetype/ttpload.c
        ${FREETYPE_DIR}/src/truetype/ttsubpix.c

        ${FREETYPE_DIR}/src/type1/t1afm.c
        ${FREETYPE_DIR}/src/type1/t1driver.c
        ${FREETYPE_DIR}/src/type1/t1gload.c
        ${FREETYPE_DIR}/src/type1/t1load.c
        ${FREETYPE_DIR}/src/type1/t1objs.c
        ${FREETYPE_DIR}/src/type1/t1parse.c

        ${FREETYPE_DIR}/src/type42/t42drivr.c
        ${FREETYPE_DIR}/src/type42/t42objs.c
        ${FREETYPE_DIR}/src/type42/t42parse.c

        ${FREETYPE_DIR}/src/winfonts/winfnt.c
)
