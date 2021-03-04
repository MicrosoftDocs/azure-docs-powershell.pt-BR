---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: e96b4360247937ace5a0e2894f3bfac19fc1da0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893078"
---
# <span data-ttu-id="bb7a6-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bb7a6-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="bb7a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7a6-103">Este comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="bb7a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bb7a6-104">SYNTAX</span></span>

### <span data-ttu-id="bb7a6-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bb7a6-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb7a6-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb7a6-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb7a6-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb7a6-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb7a6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bb7a6-108">DESCRIPTION</span></span>
<span data-ttu-id="bb7a6-109">Este comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="bb7a6-110">Um grupo de sincronização é usado para descrever uma topologia de locais, conhecida como pontos de extremidade, que sincroniza os arquivos armazenados em qualquer um dos pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="bb7a6-111">Um grupo de sincronização contém pontos de extremidade de nuvem, que referenciam compartilhamentos de arquivos do Azure, e também contém pontos de extremidade de servidor que referenciam um caminho local específico em um servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="bb7a6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb7a6-112">EXAMPLES</span></span>

### <span data-ttu-id="bb7a6-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb7a6-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="bb7a6-114">Este comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="bb7a6-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bb7a6-115">PARAMETERS</span></span>

### <span data-ttu-id="bb7a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb7a6-116">-DefaultProfile</span></span>
<span data-ttu-id="bb7a6-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb7a6-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bb7a6-118">-Name</span></span>
<span data-ttu-id="bb7a6-119">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7a6-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bb7a6-120">-ParentObject</span></span>
<span data-ttu-id="bb7a6-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7a6-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="bb7a6-122">-ParentResourceId</span></span>
<span data-ttu-id="bb7a6-123">ID de recurso pai do StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bb7a6-123">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb7a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb7a6-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7a6-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="bb7a6-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="bb7a6-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb7a6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb7a6-128">-Confirm</span></span>
<span data-ttu-id="bb7a6-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb7a6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb7a6-130">-WhatIf</span></span>
<span data-ttu-id="bb7a6-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb7a6-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb7a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb7a6-133">CommonParameters</span></span>
<span data-ttu-id="bb7a6-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb7a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb7a6-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb7a6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb7a6-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb7a6-136">INPUTS</span></span>

### <span data-ttu-id="bb7a6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="bb7a6-137">System.String</span></span>

### <span data-ttu-id="bb7a6-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="bb7a6-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="bb7a6-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bb7a6-139">OUTPUTS</span></span>

### <span data-ttu-id="bb7a6-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="bb7a6-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="bb7a6-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="bb7a6-141">NOTES</span></span>

## <span data-ttu-id="bb7a6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb7a6-142">RELATED LINKS</span></span>
