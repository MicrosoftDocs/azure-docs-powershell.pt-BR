---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117489"
---
# <span data-ttu-id="d576e-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d576e-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="d576e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d576e-102">SYNOPSIS</span></span>
<span data-ttu-id="d576e-103">Atualiza o volume de arquivos Azure NetApp (ANF) de acordo com os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="d576e-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="d576e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d576e-104">SYNTAX</span></span>

### <span data-ttu-id="d576e-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d576e-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d576e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d576e-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d576e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d576e-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d576e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d576e-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d576e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d576e-109">DESCRIPTION</span></span>
<span data-ttu-id="d576e-110">O cmdlet **Update-AzNetAppFilesVolume** atualiza um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="d576e-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="d576e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d576e-111">EXAMPLES</span></span>

### <span data-ttu-id="d576e-112">Exemplo 1: Atualizar um volume de ANF</span><span class="sxs-lookup"><span data-stu-id="d576e-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="d576e-113">Este comando atualiza o volume da ANF "MyAnfVolume" com o novo tamanho UsageThreshold.</span><span class="sxs-lookup"><span data-stu-id="d576e-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="d576e-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d576e-114">PARAMETERS</span></span>

### <span data-ttu-id="d576e-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="d576e-115">-AccountName</span></span>
<span data-ttu-id="d576e-116">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="d576e-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="d576e-117">-Backup</span><span class="sxs-lookup"><span data-stu-id="d576e-117">-Backup</span></span>
<span data-ttu-id="d576e-118">Uma matriz de tabela hash que representa o objeto de backup</span><span class="sxs-lookup"><span data-stu-id="d576e-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="d576e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d576e-119">-DefaultProfile</span></span>
<span data-ttu-id="d576e-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d576e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d576e-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="d576e-121">-ExportPolicy</span></span>
<span data-ttu-id="d576e-122">Uma matriz de tabela hash que representa a política de exportação</span><span class="sxs-lookup"><span data-stu-id="d576e-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="d576e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d576e-123">-InputObject</span></span>
<span data-ttu-id="d576e-124">O objeto de volume a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="d576e-124">The volume object to update</span></span>

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

### <span data-ttu-id="d576e-125">-Local</span><span class="sxs-lookup"><span data-stu-id="d576e-125">-Location</span></span>
<span data-ttu-id="d576e-126">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="d576e-126">The location of the resource</span></span>

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

### <span data-ttu-id="d576e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d576e-127">-Name</span></span>
<span data-ttu-id="d576e-128">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="d576e-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d576e-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d576e-129">-PoolName</span></span>
<span data-ttu-id="d576e-130">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="d576e-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d576e-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="d576e-131">-PoolObject</span></span>
<span data-ttu-id="d576e-132">O objeto de pool que contém o volume a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="d576e-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="d576e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d576e-133">-ResourceGroupName</span></span>
<span data-ttu-id="d576e-134">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="d576e-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="d576e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d576e-135">-ResourceId</span></span>
<span data-ttu-id="d576e-136">A ID do recurso do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="d576e-136">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="d576e-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="d576e-137">-ServiceLevel</span></span>
<span data-ttu-id="d576e-138">O nível de serviço do volume de ANF</span><span class="sxs-lookup"><span data-stu-id="d576e-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="d576e-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="d576e-139">-Tag</span></span>
<span data-ttu-id="d576e-140">Uma tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="d576e-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="d576e-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="d576e-141">-ThroughputMibps</span></span>
<span data-ttu-id="d576e-142">Produtividade máxima em Mibps que pode ser obtido por esse volume</span><span class="sxs-lookup"><span data-stu-id="d576e-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="d576e-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="d576e-143">-UsageThreshold</span></span>
<span data-ttu-id="d576e-144">A cota máxima de armazenamento permitida para um sistema de arquivos em bytes</span><span class="sxs-lookup"><span data-stu-id="d576e-144">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="d576e-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d576e-145">-Confirm</span></span>
<span data-ttu-id="d576e-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d576e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d576e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d576e-147">-WhatIf</span></span>
<span data-ttu-id="d576e-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d576e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d576e-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d576e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d576e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d576e-150">CommonParameters</span></span>
<span data-ttu-id="d576e-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d576e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d576e-152">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d576e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d576e-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="d576e-153">INPUTS</span></span>

### <span data-ttu-id="d576e-154">System.String</span><span class="sxs-lookup"><span data-stu-id="d576e-154">System.String</span></span>

### <span data-ttu-id="d576e-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d576e-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="d576e-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d576e-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d576e-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="d576e-157">OUTPUTS</span></span>

### <span data-ttu-id="d576e-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d576e-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d576e-159">Notas</span><span class="sxs-lookup"><span data-stu-id="d576e-159">NOTES</span></span>

## <span data-ttu-id="d576e-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d576e-160">RELATED LINKS</span></span>
