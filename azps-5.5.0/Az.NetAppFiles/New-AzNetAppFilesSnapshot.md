---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112925"
---
# <span data-ttu-id="a8946-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="a8946-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="a8946-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a8946-102">SYNOPSIS</span></span>
<span data-ttu-id="a8946-103">Cria um novo instantâneo do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="a8946-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="a8946-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8946-104">SYNTAX</span></span>

### <span data-ttu-id="a8946-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a8946-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8946-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8946-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8946-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8946-107">DESCRIPTION</span></span>
<span data-ttu-id="a8946-108">O cmdlet **New-AzNetAppFilesSnapshot** cria um instantâneo ANF.</span><span class="sxs-lookup"><span data-stu-id="a8946-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="a8946-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8946-109">EXAMPLES</span></span>

### <span data-ttu-id="a8946-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a8946-110">Example 1</span></span>
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

<span data-ttu-id="a8946-111">Esse comando cria o novo instantâneo ANF "MyAnfSnapshot" dentro do volume "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="a8946-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="a8946-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8946-112">PARAMETERS</span></span>

### <span data-ttu-id="a8946-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="a8946-113">-AccountName</span></span>
<span data-ttu-id="a8946-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="a8946-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="a8946-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8946-115">-DefaultProfile</span></span>
<span data-ttu-id="a8946-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8946-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8946-117">-FileSystemId</span><span class="sxs-lookup"><span data-stu-id="a8946-117">-FileSystemId</span></span>
<span data-ttu-id="a8946-118">A ID do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="a8946-118">The file system id</span></span>

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

### <span data-ttu-id="a8946-119">-Local</span><span class="sxs-lookup"><span data-stu-id="a8946-119">-Location</span></span>
<span data-ttu-id="a8946-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="a8946-120">The location of the resource</span></span>

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

### <span data-ttu-id="a8946-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8946-121">-Name</span></span>
<span data-ttu-id="a8946-122">O nome do instantâneo ANF</span><span class="sxs-lookup"><span data-stu-id="a8946-122">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="a8946-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a8946-123">-PoolName</span></span>
<span data-ttu-id="a8946-124">O nome do pool de ANF</span><span class="sxs-lookup"><span data-stu-id="a8946-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a8946-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8946-125">-ResourceGroupName</span></span>
<span data-ttu-id="a8946-126">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="a8946-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a8946-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8946-127">-Tag</span></span>
<span data-ttu-id="a8946-128">Uma tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="a8946-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="a8946-129">-Nomedo Volume</span><span class="sxs-lookup"><span data-stu-id="a8946-129">-VolumeName</span></span>
<span data-ttu-id="a8946-130">O nome do volume da ANF</span><span class="sxs-lookup"><span data-stu-id="a8946-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="a8946-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="a8946-131">-VolumeObject</span></span>
<span data-ttu-id="a8946-132">O volume do novo objeto de instantâneo</span><span class="sxs-lookup"><span data-stu-id="a8946-132">The volume for the new snapshot object</span></span>

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

### <span data-ttu-id="a8946-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a8946-133">-Confirm</span></span>
<span data-ttu-id="a8946-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8946-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8946-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8946-135">-WhatIf</span></span>
<span data-ttu-id="a8946-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a8946-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8946-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8946-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8946-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8946-138">CommonParameters</span></span>
<span data-ttu-id="a8946-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8946-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8946-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a8946-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8946-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="a8946-141">INPUTS</span></span>

### <span data-ttu-id="a8946-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a8946-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a8946-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="a8946-143">OUTPUTS</span></span>

### <span data-ttu-id="a8946-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="a8946-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="a8946-145">Notas</span><span class="sxs-lookup"><span data-stu-id="a8946-145">NOTES</span></span>

## <span data-ttu-id="a8946-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8946-146">RELATED LINKS</span></span>
