---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942450"
---
# <span data-ttu-id="1fb93-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1fb93-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="1fb93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fb93-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb93-103">Esse comando lista todos os grupos de sincronização em um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1fb93-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="1fb93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fb93-104">SYNTAX</span></span>

### <span data-ttu-id="1fb93-105">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1fb93-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb93-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="1fb93-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb93-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fb93-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fb93-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1fb93-108">DESCRIPTION</span></span>
<span data-ttu-id="1fb93-109">Esse comando lista todos os grupos de sincronização em um determinado serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1fb93-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="1fb93-110">Ele também pode ser usado para listar os atributos de cada grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1fb93-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="1fb93-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fb93-111">EXAMPLES</span></span>

### <span data-ttu-id="1fb93-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1fb93-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="1fb93-113">Esse comando obtém todos os grupos de sincronização contidos no serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="1fb93-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="1fb93-114">Especifique-name para retornar uma específica.</span><span class="sxs-lookup"><span data-stu-id="1fb93-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="1fb93-115">OS</span><span class="sxs-lookup"><span data-stu-id="1fb93-115">PARAMETERS</span></span>

### <span data-ttu-id="1fb93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb93-116">-DefaultProfile</span></span>
<span data-ttu-id="1fb93-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb93-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb93-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fb93-118">-Name</span></span>
<span data-ttu-id="1fb93-119">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="1fb93-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="1fb93-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1fb93-120">-ParentObject</span></span>
<span data-ttu-id="1fb93-121">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1fb93-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1fb93-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1fb93-122">-ParentResourceId</span></span>
<span data-ttu-id="1fb93-123">Objeto StorageSyncService, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1fb93-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1fb93-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb93-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fb93-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1fb93-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1fb93-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1fb93-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="1fb93-127">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1fb93-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="1fb93-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb93-128">CommonParameters</span></span>
<span data-ttu-id="1fb93-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb93-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb93-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb93-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb93-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1fb93-131">INPUTS</span></span>

### <span data-ttu-id="1fb93-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb93-132">System.String</span></span>

### <span data-ttu-id="1fb93-133">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1fb93-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="1fb93-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1fb93-134">OUTPUTS</span></span>

### <span data-ttu-id="1fb93-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1fb93-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="1fb93-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1fb93-136">NOTES</span></span>

## <span data-ttu-id="1fb93-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fb93-137">RELATED LINKS</span></span>
