---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111721"
---
# <span data-ttu-id="f4ad5-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f4ad5-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="f4ad5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ad5-103">Cria um novo volume de Arquivos Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="f4ad5-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="f4ad5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4ad5-104">SYNTAX</span></span>

### <span data-ttu-id="f4ad5-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f4ad5-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ad5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4ad5-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4ad5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4ad5-107">DESCRIPTION</span></span>
<span data-ttu-id="f4ad5-108">O **cmdlet New-AzNetAppFilesVolume** cria um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="f4ad5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f4ad5-109">EXAMPLES</span></span>

### <span data-ttu-id="f4ad5-110">Exemplo 1: Criar um volume de ANF</span><span class="sxs-lookup"><span data-stu-id="f4ad5-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="f4ad5-111">Esse comando cria o novo volume da ANF "MyAnfVolume" no pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="f4ad5-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="f4ad5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4ad5-112">PARAMETERS</span></span>

### <span data-ttu-id="f4ad5-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="f4ad5-113">-AccountName</span></span>
<span data-ttu-id="f4ad5-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="f4ad5-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="f4ad5-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="f4ad5-115">-Backup</span></span>
<span data-ttu-id="f4ad5-116">Uma matriz de tabela hash que representa o objeto de backup</span><span class="sxs-lookup"><span data-stu-id="f4ad5-116">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="f4ad5-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="f4ad5-117">-BackupId</span></span>
<span data-ttu-id="f4ad5-118">ID de backup.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-118">Backup ID.</span></span> <span data-ttu-id="f4ad5-119">UUID v4 ou identificador de recurso usado para identificar o Backup</span><span class="sxs-lookup"><span data-stu-id="f4ad5-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="f4ad5-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="f4ad5-120">-CreationToken</span></span>
<span data-ttu-id="f4ad5-121">Um caminho de arquivo exclusivo para o volume</span><span class="sxs-lookup"><span data-stu-id="f4ad5-121">A unique file path for the volume</span></span>

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

### <span data-ttu-id="f4ad5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ad5-122">-DefaultProfile</span></span>
<span data-ttu-id="f4ad5-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4ad5-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="f4ad5-124">-ExportPolicy</span></span>
<span data-ttu-id="f4ad5-125">Uma matriz de tabela hash que representa a política de exportação</span><span class="sxs-lookup"><span data-stu-id="f4ad5-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="f4ad5-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="f4ad5-126">-KerberosEnabled</span></span>
<span data-ttu-id="f4ad5-127">Descrever se um volume está Habilitado kerberos</span><span class="sxs-lookup"><span data-stu-id="f4ad5-127">Describe if a volume is Kerberos Enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad5-128">-Local</span><span class="sxs-lookup"><span data-stu-id="f4ad5-128">-Location</span></span>
<span data-ttu-id="f4ad5-129">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="f4ad5-129">The location of the resource</span></span>

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

### <span data-ttu-id="f4ad5-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4ad5-130">-Name</span></span>
<span data-ttu-id="f4ad5-131">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="f4ad5-131">The name of the ANF volume</span></span>

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

### <span data-ttu-id="f4ad5-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="f4ad5-132">-PoolName</span></span>
<span data-ttu-id="f4ad5-133">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="f4ad5-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f4ad5-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="f4ad5-134">-PoolObject</span></span>
<span data-ttu-id="f4ad5-135">O pool para o novo objeto de volume</span><span class="sxs-lookup"><span data-stu-id="f4ad5-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="f4ad5-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="f4ad5-136">-ProtocolType</span></span>
<span data-ttu-id="f4ad5-137">Uma matriz de tabela hash que representa a política de exportação</span><span class="sxs-lookup"><span data-stu-id="f4ad5-137">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="f4ad5-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="f4ad5-138">-ReplicationObject</span></span>
<span data-ttu-id="f4ad5-139">Uma matriz de tabela hash que representa o objeto de replicação</span><span class="sxs-lookup"><span data-stu-id="f4ad5-139">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="f4ad5-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4ad5-140">-ResourceGroupName</span></span>
<span data-ttu-id="f4ad5-141">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="f4ad5-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f4ad5-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="f4ad5-142">-SecurityStyle</span></span>
<span data-ttu-id="f4ad5-143">O estilo de segurança do volume.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-143">The security style of volume.</span></span> <span data-ttu-id="f4ad5-144">Os valores possíveis incluem: 'ntfs', 'unix'</span><span class="sxs-lookup"><span data-stu-id="f4ad5-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="f4ad5-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="f4ad5-145">-ServiceLevel</span></span>
<span data-ttu-id="f4ad5-146">O nível de serviço do volume de ANF</span><span class="sxs-lookup"><span data-stu-id="f4ad5-146">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="f4ad5-147">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="f4ad5-147">-Snapshot</span></span>
<span data-ttu-id="f4ad5-148">Uma matriz de tabela hash que representa o objeto de instantâneo</span><span class="sxs-lookup"><span data-stu-id="f4ad5-148">A hashtable array which represents the snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeSnapshot
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad5-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="f4ad5-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="f4ad5-150">Se habilitado (verdadeiro), o volume conterá um diretório .snapshot somente leitura que fornece acesso a cada um dos instantâneos do volume (padrão para verdadeiro)</span><span class="sxs-lookup"><span data-stu-id="f4ad5-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4ad5-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="f4ad5-151">-SnapshotId</span></span>
<span data-ttu-id="f4ad5-152">Crie volume a partir de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-152">Create volume from a snapshot.</span></span> <span data-ttu-id="f4ad5-153">UUID v4 ou identificador de recurso usado para identificar o Instantâneo</span><span class="sxs-lookup"><span data-stu-id="f4ad5-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="f4ad5-154">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="f4ad5-154">-SubnetId</span></span>
<span data-ttu-id="f4ad5-155">O URI de recurso do Azure para uma sub-rede delegada</span><span class="sxs-lookup"><span data-stu-id="f4ad5-155">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="f4ad5-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4ad5-156">-Tag</span></span>
<span data-ttu-id="f4ad5-157">Uma tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="f4ad5-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="f4ad5-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="f4ad5-158">-ThroughputMibps</span></span>
<span data-ttu-id="f4ad5-159">Produtividade máxima em Mibps que pode ser obtido por esse volume</span><span class="sxs-lookup"><span data-stu-id="f4ad5-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="f4ad5-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="f4ad5-160">-UsageThreshold</span></span>
<span data-ttu-id="f4ad5-161">A cota máxima de armazenamento permitida para um sistema de arquivos em bytes</span><span class="sxs-lookup"><span data-stu-id="f4ad5-161">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="f4ad5-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="f4ad5-162">-VolumeType</span></span>
<span data-ttu-id="f4ad5-163">O tipo de volume de ANF</span><span class="sxs-lookup"><span data-stu-id="f4ad5-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="f4ad5-164">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f4ad5-164">-Confirm</span></span>
<span data-ttu-id="f4ad5-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ad5-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ad5-166">-WhatIf</span></span>
<span data-ttu-id="f4ad5-167">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ad5-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ad5-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ad5-169">CommonParameters</span></span>
<span data-ttu-id="f4ad5-170">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ad5-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ad5-171">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4ad5-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ad5-172">Entradas</span><span class="sxs-lookup"><span data-stu-id="f4ad5-172">INPUTS</span></span>

### <span data-ttu-id="f4ad5-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="f4ad5-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="f4ad5-174">Saídas</span><span class="sxs-lookup"><span data-stu-id="f4ad5-174">OUTPUTS</span></span>

### <span data-ttu-id="f4ad5-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f4ad5-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f4ad5-176">Notas</span><span class="sxs-lookup"><span data-stu-id="f4ad5-176">NOTES</span></span>

## <span data-ttu-id="f4ad5-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4ad5-177">RELATED LINKS</span></span>
