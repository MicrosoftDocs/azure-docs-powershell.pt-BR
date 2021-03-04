---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: b7947f4224c667ed8332b0f3206588dda49fd1af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887395"
---
# <span data-ttu-id="2593a-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2593a-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="2593a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2593a-102">SYNOPSIS</span></span>
<span data-ttu-id="2593a-103">Atualiza um volume de Arquivos do Azure NetApp (ANF) de acordo com os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="2593a-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="2593a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2593a-104">SYNTAX</span></span>

### <span data-ttu-id="2593a-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2593a-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2593a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2593a-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2593a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2593a-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2593a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2593a-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2593a-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2593a-109">DESCRIPTION</span></span>
<span data-ttu-id="2593a-110">O cmdlet **Update-AzNetAppFilesVolume** atualiza um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="2593a-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="2593a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2593a-111">EXAMPLES</span></span>

### <span data-ttu-id="2593a-112">Exemplo 1: Atualizar um volume ANF</span><span class="sxs-lookup"><span data-stu-id="2593a-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="2593a-113">Este comando atualiza o volume da ANF "MyAnfVolume" com o novo tamanho UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="2593a-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="2593a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2593a-114">PARAMETERS</span></span>

### <span data-ttu-id="2593a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2593a-115">-AccountName</span></span>
<span data-ttu-id="2593a-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="2593a-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="2593a-117">-Backup</span><span class="sxs-lookup"><span data-stu-id="2593a-117">-Backup</span></span>
<span data-ttu-id="2593a-118">Uma matriz hashtable que representa o objeto de backup</span><span class="sxs-lookup"><span data-stu-id="2593a-118">A hashtable array which represents the backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeBackupProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2593a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2593a-119">-DefaultProfile</span></span>
<span data-ttu-id="2593a-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2593a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2593a-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="2593a-121">-ExportPolicy</span></span>
<span data-ttu-id="2593a-122">Uma matriz hashtable que representa a política de exportação</span><span class="sxs-lookup"><span data-stu-id="2593a-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="2593a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2593a-123">-InputObject</span></span>
<span data-ttu-id="2593a-124">O objeto volume a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="2593a-124">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2593a-125">-Location</span><span class="sxs-lookup"><span data-stu-id="2593a-125">-Location</span></span>
<span data-ttu-id="2593a-126">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="2593a-126">The location of the resource</span></span>

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

### <span data-ttu-id="2593a-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2593a-127">-Name</span></span>
<span data-ttu-id="2593a-128">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="2593a-128">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2593a-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="2593a-129">-PoolName</span></span>
<span data-ttu-id="2593a-130">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="2593a-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="2593a-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="2593a-131">-PoolObject</span></span>
<span data-ttu-id="2593a-132">O objeto pool que contém o volume a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="2593a-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="2593a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2593a-133">-ResourceGroupName</span></span>
<span data-ttu-id="2593a-134">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="2593a-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="2593a-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2593a-135">-ResourceId</span></span>
<span data-ttu-id="2593a-136">A id de recurso do volume ANF</span><span class="sxs-lookup"><span data-stu-id="2593a-136">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2593a-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="2593a-137">-ServiceLevel</span></span>
<span data-ttu-id="2593a-138">O nível de serviço do volume ANF</span><span class="sxs-lookup"><span data-stu-id="2593a-138">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2593a-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="2593a-139">-Tag</span></span>
<span data-ttu-id="2593a-140">Uma hashtable que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="2593a-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="2593a-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="2593a-141">-ThroughputMibps</span></span>
<span data-ttu-id="2593a-142">Produtividade máxima em Mibps que pode ser atingida por esse volume</span><span class="sxs-lookup"><span data-stu-id="2593a-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2593a-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="2593a-143">-UsageThreshold</span></span>
<span data-ttu-id="2593a-144">A cota máxima de armazenamento permitida para um sistema de arquivos em bytes</span><span class="sxs-lookup"><span data-stu-id="2593a-144">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2593a-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2593a-145">-Confirm</span></span>
<span data-ttu-id="2593a-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2593a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2593a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2593a-147">-WhatIf</span></span>
<span data-ttu-id="2593a-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2593a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2593a-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2593a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2593a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2593a-150">CommonParameters</span></span>
<span data-ttu-id="2593a-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2593a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2593a-152">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2593a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2593a-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2593a-153">INPUTS</span></span>

### <span data-ttu-id="2593a-154">System.String</span><span class="sxs-lookup"><span data-stu-id="2593a-154">System.String</span></span>

### <span data-ttu-id="2593a-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="2593a-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="2593a-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2593a-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2593a-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2593a-157">OUTPUTS</span></span>

### <span data-ttu-id="2593a-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="2593a-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="2593a-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="2593a-159">NOTES</span></span>

## <span data-ttu-id="2593a-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2593a-160">RELATED LINKS</span></span>
