---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114168"
---
# <span data-ttu-id="713f5-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="713f5-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="713f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="713f5-102">SYNOPSIS</span></span>
<span data-ttu-id="713f5-103">Cria um novo instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="713f5-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="713f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="713f5-104">SYNTAX</span></span>

### <span data-ttu-id="713f5-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="713f5-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="713f5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="713f5-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="713f5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="713f5-107">DESCRIPTION</span></span>
<span data-ttu-id="713f5-108">O cmdlet **New-AzNetAppFilesSnapshot** cria um instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="713f5-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="713f5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="713f5-109">EXAMPLES</span></span>

### <span data-ttu-id="713f5-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="713f5-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="713f5-111">Esse comando cria o novo instantâneo ANF "MyAnfSnapshot" dentro do volume "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="713f5-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="713f5-112">OS</span><span class="sxs-lookup"><span data-stu-id="713f5-112">PARAMETERS</span></span>

### <span data-ttu-id="713f5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="713f5-113">-AccountName</span></span>
<span data-ttu-id="713f5-114">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="713f5-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="713f5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="713f5-115">-DefaultProfile</span></span>
<span data-ttu-id="713f5-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="713f5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="713f5-117">-Filesystemid</span><span class="sxs-lookup"><span data-stu-id="713f5-117">-FileSystemId</span></span>
<span data-ttu-id="713f5-118">A ID do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="713f5-118">The file system id</span></span>

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

### <span data-ttu-id="713f5-119">-Local</span><span class="sxs-lookup"><span data-stu-id="713f5-119">-Location</span></span>
<span data-ttu-id="713f5-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="713f5-120">The location of the resource</span></span>

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

### <span data-ttu-id="713f5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="713f5-121">-Name</span></span>
<span data-ttu-id="713f5-122">O nome do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="713f5-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="713f5-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="713f5-123">-PoolName</span></span>
<span data-ttu-id="713f5-124">O nome do pool ANF</span><span class="sxs-lookup"><span data-stu-id="713f5-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="713f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="713f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="713f5-126">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="713f5-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="713f5-127">-Marca</span><span class="sxs-lookup"><span data-stu-id="713f5-127">-Tag</span></span>
<span data-ttu-id="713f5-128">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="713f5-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="713f5-129">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="713f5-129">-VolumeName</span></span>
<span data-ttu-id="713f5-130">O nome do volume ANF</span><span class="sxs-lookup"><span data-stu-id="713f5-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="713f5-131">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="713f5-131">-VolumeObject</span></span>
<span data-ttu-id="713f5-132">O volume do novo objeto de instantâneo</span><span class="sxs-lookup"><span data-stu-id="713f5-132">The volume for the new snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="713f5-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="713f5-133">-Confirm</span></span>
<span data-ttu-id="713f5-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="713f5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="713f5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="713f5-135">-WhatIf</span></span>
<span data-ttu-id="713f5-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="713f5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="713f5-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="713f5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="713f5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="713f5-138">CommonParameters</span></span>
<span data-ttu-id="713f5-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="713f5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="713f5-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="713f5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="713f5-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="713f5-141">INPUTS</span></span>

### <span data-ttu-id="713f5-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="713f5-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="713f5-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="713f5-143">OUTPUTS</span></span>

### <span data-ttu-id="713f5-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="713f5-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="713f5-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="713f5-145">NOTES</span></span>

## <span data-ttu-id="713f5-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="713f5-146">RELATED LINKS</span></span>
