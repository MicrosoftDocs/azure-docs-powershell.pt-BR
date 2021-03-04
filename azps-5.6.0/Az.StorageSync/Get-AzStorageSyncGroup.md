---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: 53ee755daeb0e483b98c9e8449720acce6e38233
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888031"
---
# <span data-ttu-id="b9c6c-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b9c6c-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="b9c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c6c-103">Este comando lista todos os grupos de sincronização em um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="b9c6c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b9c6c-104">SYNTAX</span></span>

### <span data-ttu-id="b9c6c-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b9c6c-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c6c-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c6c-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c6c-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c6c-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9c6c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b9c6c-108">DESCRIPTION</span></span>
<span data-ttu-id="b9c6c-109">Este comando lista todos os grupos de sincronização em um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="b9c6c-110">Ele também pode ser usado para listar os atributos de cada grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="b9c6c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9c6c-111">EXAMPLES</span></span>

### <span data-ttu-id="b9c6c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9c6c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="b9c6c-113">Esse comando obtém todos os grupos de sincronização contidos no serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="b9c6c-114">Especifique -Name para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="b9c6c-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b9c6c-115">PARAMETERS</span></span>

### <span data-ttu-id="b9c6c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c6c-116">-DefaultProfile</span></span>
<span data-ttu-id="b9c6c-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c6c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b9c6c-118">-Name</span></span>
<span data-ttu-id="b9c6c-119">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c6c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b9c6c-120">-ParentObject</span></span>
<span data-ttu-id="b9c6c-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b9c6c-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b9c6c-122">-ParentResourceId</span></span>
<span data-ttu-id="b9c6c-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b9c6c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c6c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9c6c-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b9c6c-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b9c6c-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="b9c6c-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b9c6c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c6c-128">CommonParameters</span></span>
<span data-ttu-id="b9c6c-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c6c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c6c-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c6c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c6c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9c6c-131">INPUTS</span></span>

### <span data-ttu-id="b9c6c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b9c6c-132">System.String</span></span>

### <span data-ttu-id="b9c6c-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b9c6c-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b9c6c-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b9c6c-134">OUTPUTS</span></span>

### <span data-ttu-id="b9c6c-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b9c6c-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="b9c6c-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="b9c6c-136">NOTES</span></span>

## <span data-ttu-id="b9c6c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9c6c-137">RELATED LINKS</span></span>
