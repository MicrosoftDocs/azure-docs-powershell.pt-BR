---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945515"
---
# <span data-ttu-id="6fd23-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="6fd23-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="6fd23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fd23-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd23-103">Prepara um objeto de configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="6fd23-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="6fd23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fd23-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6fd23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fd23-105">DESCRIPTION</span></span>
<span data-ttu-id="6fd23-106">O cmdlet **New-AzureStorSimpleNetworkConfig** prepara um objeto de configuração de rede para passar para o cmdlet **set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="6fd23-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="6fd23-107">Defina o parâmetro *Controller0IPAddress* e o parâmetro *Controller1IPAddress* apenas na interface Data0.</span><span class="sxs-lookup"><span data-stu-id="6fd23-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="6fd23-108">O Data0 dá suporte a apenas três configurações: *Controller0IPAddress* , *Controller1IPAdress* e *EnableIscsi*.</span><span class="sxs-lookup"><span data-stu-id="6fd23-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="6fd23-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fd23-109">EXAMPLES</span></span>

### <span data-ttu-id="6fd23-110">Exemplo 1: configurar uma interface Data0</span><span class="sxs-lookup"><span data-stu-id="6fd23-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="6fd23-111">Esse comando cria a configuração de rede para a interface Data0.</span><span class="sxs-lookup"><span data-stu-id="6fd23-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="6fd23-112">Esse comando especifica os parâmetros *Controller0IPv4Address* , *Controller1IPv4Address* e *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="6fd23-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="6fd23-113">Este cmdlet pode configurar o Data0 para apenas esses três parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6fd23-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="6fd23-114">Exemplo 2: configurar uma interface diferente de Data0 um</span><span class="sxs-lookup"><span data-stu-id="6fd23-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="6fd23-115">Esse comando configura a interface Dados1.</span><span class="sxs-lookup"><span data-stu-id="6fd23-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="6fd23-116">Exemplo 3: modificar uma configuração para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="6fd23-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="6fd23-117">O primeiro comando cria uma configuração de rede para a interface Data0.</span><span class="sxs-lookup"><span data-stu-id="6fd23-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="6fd23-118">Esse comando especifica os parâmetros *Controller0IPv4Address* , *Controller1IPv4Address* e *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="6fd23-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="6fd23-119">O comando armazena o resultado na variável $NetworkConfigData 0.</span><span class="sxs-lookup"><span data-stu-id="6fd23-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="6fd23-120">O segundo comando usa o cmdlet **Get-AzureStorSimpleDevice** e o cmdlet de núcleo do **objeto Where** para obter um dispositivo StorSimple online e, em seguida, armazena-o na variável $OnlineDevice.</span><span class="sxs-lookup"><span data-stu-id="6fd23-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="6fd23-121">O comando final modifica a configuração do dispositivo que tem a identificação de dispositivo especificada usando o cmdlet **set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="6fd23-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="6fd23-122">O comando usa o objeto de configuração que o cmdlet atual criou no primeiro comando.</span><span class="sxs-lookup"><span data-stu-id="6fd23-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="6fd23-123">OS</span><span class="sxs-lookup"><span data-stu-id="6fd23-123">PARAMETERS</span></span>

### <span data-ttu-id="6fd23-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="6fd23-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="6fd23-125">Especifica o endereço IPv4 para o controlador 0.</span><span class="sxs-lookup"><span data-stu-id="6fd23-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="6fd23-126">Especifique esse parâmetro somente para a interface Data0.</span><span class="sxs-lookup"><span data-stu-id="6fd23-126">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="6fd23-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="6fd23-128">Especifica o endereço IPv4 para o controlador 1.</span><span class="sxs-lookup"><span data-stu-id="6fd23-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="6fd23-129">Especifique esse parâmetro somente para a interface Data0.</span><span class="sxs-lookup"><span data-stu-id="6fd23-129">Specify this parameter only for the Data0 interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="6fd23-130">-EnableCloud</span></span>
<span data-ttu-id="6fd23-131">Indica se a interface será habilitada na nuvem.</span><span class="sxs-lookup"><span data-stu-id="6fd23-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-132">-EnableIscsi</span><span class="sxs-lookup"><span data-stu-id="6fd23-132">-EnableIscsi</span></span>
<span data-ttu-id="6fd23-133">Indica se o SCSI da Internet (ISCSI) deve ser habilitado para a interface.</span><span class="sxs-lookup"><span data-stu-id="6fd23-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-134">-InterfaceAlias</span><span class="sxs-lookup"><span data-stu-id="6fd23-134">-InterfaceAlias</span></span>
<span data-ttu-id="6fd23-135">Especifica o alias da interface para o qual este cmdlet fornece configurações.</span><span class="sxs-lookup"><span data-stu-id="6fd23-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="6fd23-136">Os valores válidos são de Data0 para data5.</span><span class="sxs-lookup"><span data-stu-id="6fd23-136">Valid values are from Data0 to Data5.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-137">-IPv4Address</span><span class="sxs-lookup"><span data-stu-id="6fd23-137">-IPv4Address</span></span>
<span data-ttu-id="6fd23-138">Especifica o endereço IPv4 para a interface.</span><span class="sxs-lookup"><span data-stu-id="6fd23-138">Specifies the IPv4 address for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="6fd23-139">-IPv4Gateway</span></span>
<span data-ttu-id="6fd23-140">Especifica o endereço IPv4 de um gateway.</span><span class="sxs-lookup"><span data-stu-id="6fd23-140">Specifies the IPv4 address of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="6fd23-141">-IPv4Netmask</span></span>
<span data-ttu-id="6fd23-142">Especifica a máscara de rede IPv4 para a interface.</span><span class="sxs-lookup"><span data-stu-id="6fd23-142">Specifies the IPv4 netmask for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="6fd23-143">-IPv6Gateway</span></span>
<span data-ttu-id="6fd23-144">Especifica o gateway IPv6 para a interface.</span><span class="sxs-lookup"><span data-stu-id="6fd23-144">Specifies the IPv6 gateway for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="6fd23-145">-IPv6Prefix</span></span>
<span data-ttu-id="6fd23-146">Especifica o prefixo IPv6 para a interface.</span><span class="sxs-lookup"><span data-stu-id="6fd23-146">Specifies the IPv6 prefix for the interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-147">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6fd23-147">-Profile</span></span>
<span data-ttu-id="6fd23-148">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd23-148">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fd23-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd23-149">CommonParameters</span></span>
<span data-ttu-id="6fd23-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd23-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd23-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd23-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd23-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fd23-152">INPUTS</span></span>

### <span data-ttu-id="6fd23-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6fd23-153">None</span></span>

## <span data-ttu-id="6fd23-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fd23-154">OUTPUTS</span></span>

### <span data-ttu-id="6fd23-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="6fd23-155">NetworkConfig</span></span>
<span data-ttu-id="6fd23-156">Esse cmdlet retorna um objeto NetworkConfig que contém as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="6fd23-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="6fd23-157">**IsIscsiEnabled** ( **booliano** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="6fd23-158">**IsCloudEnabled** ( **booliano** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="6fd23-159">**Controller0IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6fd23-160">**Controller1IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6fd23-161">**IPv6Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6fd23-162">**IPv4Gateway** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6fd23-163">**IPv4Address** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6fd23-164">**IPv6Prefix** ( **cadeia de caracteres** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="6fd23-165">**IPv4Netmask** ( **IPAddress** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="6fd23-166">**InterfaceAlias** ( **netinterfaceid** )</span><span class="sxs-lookup"><span data-stu-id="6fd23-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="6fd23-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fd23-167">NOTES</span></span>

## <span data-ttu-id="6fd23-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fd23-168">RELATED LINKS</span></span>

[<span data-ttu-id="6fd23-169">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="6fd23-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="6fd23-170">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="6fd23-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


