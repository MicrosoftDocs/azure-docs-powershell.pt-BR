---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112486"
---
# <span data-ttu-id="96a4e-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96a4e-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="96a4e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="96a4e-103">Esse comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="96a4e-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="96a4e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96a4e-104">SYNTAX</span></span>

### <span data-ttu-id="96a4e-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96a4e-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a4e-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a4e-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96a4e-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="96a4e-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96a4e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="96a4e-108">DESCRIPTION</span></span>
<span data-ttu-id="96a4e-109">Esse comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="96a4e-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="96a4e-110">Um grupo de sincronização é usado para descrever uma topologia de locais, chamados de pontos de extremidade, que sincroniza os arquivos armazenados em qualquer um dos pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="96a4e-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="96a4e-111">Um grupo de sincronização contém pontos de extremidade de nuvem, que referenciam compartilhamentos de arquivos do Azure, e também contém pontos de extremidade de servidor que referenciam um caminho local específico em um servidor registrado.</span><span class="sxs-lookup"><span data-stu-id="96a4e-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="96a4e-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96a4e-112">EXAMPLES</span></span>

### <span data-ttu-id="96a4e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96a4e-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="96a4e-114">Esse comando cria um novo grupo de sincronização dentro de um serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="96a4e-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="96a4e-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96a4e-115">PARAMETERS</span></span>

### <span data-ttu-id="96a4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96a4e-116">-DefaultProfile</span></span>
<span data-ttu-id="96a4e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96a4e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96a4e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="96a4e-118">-Name</span></span>
<span data-ttu-id="96a4e-119">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="96a4e-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="96a4e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="96a4e-120">-ParentObject</span></span>
<span data-ttu-id="96a4e-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="96a4e-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="96a4e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="96a4e-122">-ParentResourceId</span></span>
<span data-ttu-id="96a4e-123">ID do Recurso Pai do StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="96a4e-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="96a4e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96a4e-124">-ResourceGroupName</span></span>
<span data-ttu-id="96a4e-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96a4e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="96a4e-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="96a4e-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="96a4e-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="96a4e-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="96a4e-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="96a4e-128">-Confirm</span></span>
<span data-ttu-id="96a4e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96a4e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96a4e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96a4e-130">-WhatIf</span></span>
<span data-ttu-id="96a4e-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="96a4e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96a4e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96a4e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96a4e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96a4e-133">CommonParameters</span></span>
<span data-ttu-id="96a4e-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96a4e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96a4e-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96a4e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96a4e-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="96a4e-136">INPUTS</span></span>

### <span data-ttu-id="96a4e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="96a4e-137">System.String</span></span>

### <span data-ttu-id="96a4e-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="96a4e-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="96a4e-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="96a4e-139">OUTPUTS</span></span>

### <span data-ttu-id="96a4e-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96a4e-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="96a4e-141">Notas</span><span class="sxs-lookup"><span data-stu-id="96a4e-141">NOTES</span></span>

## <span data-ttu-id="96a4e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96a4e-142">RELATED LINKS</span></span>
