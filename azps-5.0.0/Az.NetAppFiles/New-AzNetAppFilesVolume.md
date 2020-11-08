---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: dce91ee25cac4a716dc604e38f1ac38e5a3f3f1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118389"
---
# <span data-ttu-id="61e3a-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="61e3a-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="61e3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="61e3a-103">Cria um novo volume de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="61e3a-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="61e3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61e3a-104">SYNTAX</span></span>

### <span data-ttu-id="61e3a-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="61e3a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61e3a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61e3a-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61e3a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="61e3a-108">O cmdlet **New-AzNetAppFilesVolume** cria um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="61e3a-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="61e3a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61e3a-109">EXAMPLES</span></span>

### <span data-ttu-id="61e3a-110">Exemplo 1: criar um volume do ANF</span><span class="sxs-lookup"><span data-stu-id="61e3a-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="61e3a-111">Esse comando cria o novo volume ANF "MyAnfVolume" no pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="61e3a-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="61e3a-112">OS</span><span class="sxs-lookup"><span data-stu-id="61e3a-112">PARAMETERS</span></span>

### <span data-ttu-id="61e3a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61e3a-113">-AccountName</span></span>
<span data-ttu-id="61e3a-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="61e3a-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="61e3a-115">-CreationToken</span></span>
<span data-ttu-id="61e3a-116">Um caminho de arquivo exclusivo para o volume</span><span class="sxs-lookup"><span data-stu-id="61e3a-116">A unique file path for the volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e3a-117">-DefaultProfile</span></span>
<span data-ttu-id="61e3a-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61e3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="61e3a-119">-ExportPolicy</span></span>
<span data-ttu-id="61e3a-120">Uma matriz de Hashtable que representa a política de exportação</span><span class="sxs-lookup"><span data-stu-id="61e3a-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-121">-Local</span><span class="sxs-lookup"><span data-stu-id="61e3a-121">-Location</span></span>
<span data-ttu-id="61e3a-122">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="61e3a-122">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="61e3a-123">-Name</span></span>
<span data-ttu-id="61e3a-124">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="61e3a-124">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="61e3a-125">-PoolName</span></span>
<span data-ttu-id="61e3a-126">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="61e3a-126">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="61e3a-127">-PoolObject</span></span>
<span data-ttu-id="61e3a-128">O pool para o novo objeto de volume</span><span class="sxs-lookup"><span data-stu-id="61e3a-128">The pool for the new volume object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="61e3a-129">-ProtocolType</span></span>
<span data-ttu-id="61e3a-130">Uma matriz de Hashtable que representa a política de exportação</span><span class="sxs-lookup"><span data-stu-id="61e3a-130">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-131">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="61e3a-131">-ReplicationObject</span></span>
<span data-ttu-id="61e3a-132">Uma matriz de Hashtable que representa o objeto de replicação</span><span class="sxs-lookup"><span data-stu-id="61e3a-132">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e3a-133">-ResourceGroupName</span></span>
<span data-ttu-id="61e3a-134">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="61e3a-134">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-135">-Nível de</span><span class="sxs-lookup"><span data-stu-id="61e3a-135">-ServiceLevel</span></span>
<span data-ttu-id="61e3a-136">O nível de serviço do volume ANF</span><span class="sxs-lookup"><span data-stu-id="61e3a-136">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-137">-Captura de imagem</span><span class="sxs-lookup"><span data-stu-id="61e3a-137">-SnapshotId</span></span>
<span data-ttu-id="61e3a-138">Criar volume a partir de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="61e3a-138">Create volume from a snapshot.</span></span> <span data-ttu-id="61e3a-139">UUID v4 ou identificador de recurso usado para identificar o instantâneo</span><span class="sxs-lookup"><span data-stu-id="61e3a-139">UUID v4 or resource identifier used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-140">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="61e3a-140">-SubnetId</span></span>
<span data-ttu-id="61e3a-141">O URI do recurso do Azure para uma sub-rede delegada</span><span class="sxs-lookup"><span data-stu-id="61e3a-141">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="61e3a-142">-Tag</span></span>
<span data-ttu-id="61e3a-143">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="61e3a-143">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-144">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="61e3a-144">-UsageThreshold</span></span>
<span data-ttu-id="61e3a-145">A cota máxima de armazenamento permitida para um sistema de arquivos em bytes</span><span class="sxs-lookup"><span data-stu-id="61e3a-145">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-146">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="61e3a-146">-VolumeType</span></span>
<span data-ttu-id="61e3a-147">O tipo do volume ANF</span><span class="sxs-lookup"><span data-stu-id="61e3a-147">The type of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="61e3a-148">-Confirm</span></span>
<span data-ttu-id="61e3a-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61e3a-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e3a-150">-WhatIf</span></span>
<span data-ttu-id="61e3a-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61e3a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61e3a-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61e3a-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e3a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e3a-153">CommonParameters</span></span>
<span data-ttu-id="61e3a-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e3a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e3a-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61e3a-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e3a-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61e3a-156">INPUTS</span></span>

### <span data-ttu-id="61e3a-157">System. String</span><span class="sxs-lookup"><span data-stu-id="61e3a-157">System.String</span></span>

### <span data-ttu-id="61e3a-158">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="61e3a-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="61e3a-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61e3a-159">OUTPUTS</span></span>

### <span data-ttu-id="61e3a-160">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="61e3a-160">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="61e3a-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61e3a-161">NOTES</span></span>

## <span data-ttu-id="61e3a-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61e3a-162">RELATED LINKS</span></span>
