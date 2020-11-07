---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945776"
---
# <span data-ttu-id="919fa-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="919fa-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="919fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="919fa-102">SYNOPSIS</span></span>
<span data-ttu-id="919fa-103">Inicia uma operação de failover de grupos de contêineres de volume.</span><span class="sxs-lookup"><span data-stu-id="919fa-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="919fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="919fa-104">SYNTAX</span></span>

### <span data-ttu-id="919fa-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="919fa-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="919fa-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="919fa-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="919fa-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="919fa-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="919fa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="919fa-108">DESCRIPTION</span></span>
<span data-ttu-id="919fa-109">O cmdlet **Start-AzureStorSimpleDeviceFailoverJob** inicia uma operação de failover de um ou mais grupos de contêineres de volume de um dispositivo para outro.</span><span class="sxs-lookup"><span data-stu-id="919fa-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="919fa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="919fa-110">EXAMPLES</span></span>

### <span data-ttu-id="919fa-111">Exemplo 1: iniciar um trabalho de failover para um dispositivo nomeado e um dispositivo de destino nomeado</span><span class="sxs-lookup"><span data-stu-id="919fa-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="919fa-112">Esse comando obtém os contêineres de volume de failover para o dispositivo chamado ChewD_App7 usando o cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** .</span><span class="sxs-lookup"><span data-stu-id="919fa-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="919fa-113">O comando passa os resultados para o cmdlet **Where-Object** , que descarta os contêineres que têm um valor diferente de $true para a propriedade **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="919fa-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="919fa-114">Para obter mais informações, digite `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="919fa-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="919fa-115">O cmdlet atual inicia trabalhos de failover para os contêineres de volume de failover restantes.</span><span class="sxs-lookup"><span data-stu-id="919fa-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="919fa-116">O comando especifica o nome do dispositivo e o nome do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="919fa-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="919fa-117">O comando retorna a ID da instância do trabalho que o cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="919fa-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="919fa-118">Exemplo 2: iniciar um trabalho de failover para um dispositivo e um dispositivo de destino especificado por ID</span><span class="sxs-lookup"><span data-stu-id="919fa-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="919fa-119">Esse comando obtém os contêineres de volume de failover para o dispositivo chamado ChewD_App7 usando **Get-AzureStorSimpleFailoverVolumeContainers**.</span><span class="sxs-lookup"><span data-stu-id="919fa-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="919fa-120">O comando passa os resultados para **Where-Object** , que descarta os Conquerors que têm um valor diferente de $true para a propriedade **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="919fa-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="919fa-121">O cmdlet passa os resultados para o cmdlet **Select-Object** , que seleciona o primeiro objeto para passar para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="919fa-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="919fa-122">Para obter mais informações, digite `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="919fa-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="919fa-123">O cmdlet atual inicia trabalhos de failover para o contêiner de volume de failover selecionado.</span><span class="sxs-lookup"><span data-stu-id="919fa-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="919fa-124">O comando especifica a ID do dispositivo e a ID do dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="919fa-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="919fa-125">O comando retorna a ID da instância do trabalho que o cmdlet inicia.</span><span class="sxs-lookup"><span data-stu-id="919fa-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="919fa-126">OS</span><span class="sxs-lookup"><span data-stu-id="919fa-126">PARAMETERS</span></span>

### <span data-ttu-id="919fa-127">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="919fa-127">-DeviceId</span></span>
<span data-ttu-id="919fa-128">Especifica a ID de instância do dispositivo StorSimple no qual os grupos de contêineres de volume existem.</span><span class="sxs-lookup"><span data-stu-id="919fa-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919fa-129">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="919fa-129">-DeviceName</span></span>
<span data-ttu-id="919fa-130">Especifica o nome do dispositivo StorSimple no qual os grupos de contêineres de volume existem.</span><span class="sxs-lookup"><span data-stu-id="919fa-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919fa-131">-Force</span><span class="sxs-lookup"><span data-stu-id="919fa-131">-Force</span></span>
<span data-ttu-id="919fa-132">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="919fa-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919fa-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="919fa-133">-Profile</span></span>
<span data-ttu-id="919fa-134">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="919fa-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="919fa-135">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="919fa-135">-TargetDeviceId</span></span>
<span data-ttu-id="919fa-136">Especifica a ID de instância do dispositivo StorSimple para o qual esse cmdlet falha em grupos de contêineres de volume.</span><span class="sxs-lookup"><span data-stu-id="919fa-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919fa-137">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="919fa-137">-TargetDeviceName</span></span>
<span data-ttu-id="919fa-138">Especifica o nome do dispositivo StorSimple para o qual esse cmdlet falha em grupos de contêineres de volume.</span><span class="sxs-lookup"><span data-stu-id="919fa-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919fa-139">-VolumecontainerGroups</span><span class="sxs-lookup"><span data-stu-id="919fa-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="919fa-140">Especifica a lista de grupos de contêineres de volume para os quais este cmdlet executa failover em outro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="919fa-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="919fa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919fa-141">CommonParameters</span></span>
<span data-ttu-id="919fa-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919fa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919fa-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="919fa-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919fa-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="919fa-144">INPUTS</span></span>

### <span data-ttu-id="919fa-145">Programação\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="919fa-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="919fa-146">Você pode canalizar uma lista de grupos de contêineres de volume para este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="919fa-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="919fa-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="919fa-147">OUTPUTS</span></span>

### <span data-ttu-id="919fa-148">String</span><span class="sxs-lookup"><span data-stu-id="919fa-148">String</span></span>

## <span data-ttu-id="919fa-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="919fa-149">NOTES</span></span>

## <span data-ttu-id="919fa-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="919fa-150">RELATED LINKS</span></span>

[<span data-ttu-id="919fa-151">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="919fa-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)


