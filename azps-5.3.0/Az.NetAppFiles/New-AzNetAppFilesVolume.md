---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433508"
---
# <span data-ttu-id="01a25-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="01a25-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="01a25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01a25-102">SYNOPSIS</span></span>
<span data-ttu-id="01a25-103">Cria um novo volume de arquivos do Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="01a25-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="01a25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01a25-104">SYNTAX</span></span>

### <span data-ttu-id="01a25-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="01a25-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a25-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01a25-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01a25-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01a25-107">DESCRIPTION</span></span>
<span data-ttu-id="01a25-108">O cmdlet **New-AzNetAppFilesVolume** cria um volume ANF.</span><span class="sxs-lookup"><span data-stu-id="01a25-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="01a25-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01a25-109">EXAMPLES</span></span>

### <span data-ttu-id="01a25-110">Exemplo 1: criar um volume do ANF</span><span class="sxs-lookup"><span data-stu-id="01a25-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="01a25-111">Esse comando cria o novo volume ANF "MyAnfVolume" no pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="01a25-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="01a25-112">OS</span><span class="sxs-lookup"><span data-stu-id="01a25-112">PARAMETERS</span></span>

### <span data-ttu-id="01a25-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="01a25-113">-AccountName</span></span>
<span data-ttu-id="01a25-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="01a25-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="01a25-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="01a25-115">-Backup</span></span>
<span data-ttu-id="01a25-116">Uma matriz de Hashtable que representa o objeto backup</span><span class="sxs-lookup"><span data-stu-id="01a25-116">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="01a25-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="01a25-117">-BackupId</span></span>
<span data-ttu-id="01a25-118">ID de backup.</span><span class="sxs-lookup"><span data-stu-id="01a25-118">Backup ID.</span></span> <span data-ttu-id="01a25-119">UUID v4 ou identificador de recurso usado para identificar o backup</span><span class="sxs-lookup"><span data-stu-id="01a25-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="01a25-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="01a25-120">-CreationToken</span></span>
<span data-ttu-id="01a25-121">Um caminho de arquivo exclusivo para o volume</span><span class="sxs-lookup"><span data-stu-id="01a25-121">A unique file path for the volume</span></span>

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

### <span data-ttu-id="01a25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a25-122">-DefaultProfile</span></span>
<span data-ttu-id="01a25-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01a25-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01a25-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="01a25-124">-ExportPolicy</span></span>
<span data-ttu-id="01a25-125">Uma matriz de Hashtable que representa a política de exportação</span><span class="sxs-lookup"><span data-stu-id="01a25-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="01a25-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="01a25-126">-KerberosEnabled</span></span>
<span data-ttu-id="01a25-127">Descrever se um volume está habilitado para Kerberos</span><span class="sxs-lookup"><span data-stu-id="01a25-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="01a25-128">-Local</span><span class="sxs-lookup"><span data-stu-id="01a25-128">-Location</span></span>
<span data-ttu-id="01a25-129">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="01a25-129">The location of the resource</span></span>

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

### <span data-ttu-id="01a25-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="01a25-130">-Name</span></span>
<span data-ttu-id="01a25-131">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="01a25-131">The name of the ANF volume</span></span>

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

### <span data-ttu-id="01a25-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="01a25-132">-PoolName</span></span>
<span data-ttu-id="01a25-133">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="01a25-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="01a25-134">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="01a25-134">-PoolObject</span></span>
<span data-ttu-id="01a25-135">O pool para o novo objeto de volume</span><span class="sxs-lookup"><span data-stu-id="01a25-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="01a25-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="01a25-136">-ProtocolType</span></span>
<span data-ttu-id="01a25-137">Uma matriz de Hashtable que representa a política de exportação</span><span class="sxs-lookup"><span data-stu-id="01a25-137">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="01a25-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="01a25-138">-ReplicationObject</span></span>
<span data-ttu-id="01a25-139">Uma matriz de Hashtable que representa o objeto de replicação</span><span class="sxs-lookup"><span data-stu-id="01a25-139">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="01a25-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a25-140">-ResourceGroupName</span></span>
<span data-ttu-id="01a25-141">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="01a25-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="01a25-142">-Securitystyle</span><span class="sxs-lookup"><span data-stu-id="01a25-142">-SecurityStyle</span></span>
<span data-ttu-id="01a25-143">O estilo de segurança do volume.</span><span class="sxs-lookup"><span data-stu-id="01a25-143">The security style of volume.</span></span> <span data-ttu-id="01a25-144">Os valores possíveis incluem: ' NTFS ', ' UNIX '</span><span class="sxs-lookup"><span data-stu-id="01a25-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="01a25-145">-Nível de</span><span class="sxs-lookup"><span data-stu-id="01a25-145">-ServiceLevel</span></span>
<span data-ttu-id="01a25-146">O nível de serviço do volume ANF</span><span class="sxs-lookup"><span data-stu-id="01a25-146">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="01a25-147">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="01a25-147">-Snapshot</span></span>
<span data-ttu-id="01a25-148">Uma matriz de Hashtable que representa o objeto de instantâneo</span><span class="sxs-lookup"><span data-stu-id="01a25-148">A hashtable array which represents the snapshot object</span></span>

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

### <span data-ttu-id="01a25-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="01a25-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="01a25-150">Se habilitado (verdadeiro), o volume conterá um diretório somente leitura. diretório de instantâneo que fornece acesso a cada um dos instantâneos do volume (padrão para verdadeiro)</span><span class="sxs-lookup"><span data-stu-id="01a25-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="01a25-151">-Captura de imagem</span><span class="sxs-lookup"><span data-stu-id="01a25-151">-SnapshotId</span></span>
<span data-ttu-id="01a25-152">Criar volume a partir de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="01a25-152">Create volume from a snapshot.</span></span> <span data-ttu-id="01a25-153">UUID v4 ou identificador de recurso usado para identificar o instantâneo</span><span class="sxs-lookup"><span data-stu-id="01a25-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="01a25-154">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="01a25-154">-SubnetId</span></span>
<span data-ttu-id="01a25-155">O URI do recurso do Azure para uma sub-rede delegada</span><span class="sxs-lookup"><span data-stu-id="01a25-155">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="01a25-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="01a25-156">-Tag</span></span>
<span data-ttu-id="01a25-157">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="01a25-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="01a25-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="01a25-158">-ThroughputMibps</span></span>
<span data-ttu-id="01a25-159">Throughput máximo em Mibps que pode ser obtido por meio deste volume</span><span class="sxs-lookup"><span data-stu-id="01a25-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="01a25-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="01a25-160">-UsageThreshold</span></span>
<span data-ttu-id="01a25-161">A cota máxima de armazenamento permitida para um sistema de arquivos em bytes</span><span class="sxs-lookup"><span data-stu-id="01a25-161">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="01a25-162">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="01a25-162">-VolumeType</span></span>
<span data-ttu-id="01a25-163">O tipo do volume ANF</span><span class="sxs-lookup"><span data-stu-id="01a25-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="01a25-164">-Confirme</span><span class="sxs-lookup"><span data-stu-id="01a25-164">-Confirm</span></span>
<span data-ttu-id="01a25-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01a25-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01a25-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01a25-166">-WhatIf</span></span>
<span data-ttu-id="01a25-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01a25-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01a25-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01a25-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01a25-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a25-169">CommonParameters</span></span>
<span data-ttu-id="01a25-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01a25-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a25-171">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01a25-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a25-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01a25-172">INPUTS</span></span>

### <span data-ttu-id="01a25-173">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="01a25-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="01a25-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01a25-174">OUTPUTS</span></span>

### <span data-ttu-id="01a25-175">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="01a25-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="01a25-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01a25-176">NOTES</span></span>

## <span data-ttu-id="01a25-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01a25-177">RELATED LINKS</span></span>
