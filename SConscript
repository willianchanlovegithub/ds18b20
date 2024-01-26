from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()

# add ds18b20 src files.
if GetDepend('PKG_USING_DS18B20'):
    src += Glob('src/sensor_dallas_ds18b20.c')

if GetDepend('PKG_USING_DS18B20_SAMPLE'):
    src += Glob('sample/ds18b20_sample.c')

# add ds18b20 include path.
path  = [cwd + '/inc'] + [cwd + '/../../rt-thread/components/drivers/include/drivers']

# add src and include to group.
group = DefineGroup('ds18b20', src, depend = ['PKG_USING_DS18B20'], CPPPATH = path)

Return('group')