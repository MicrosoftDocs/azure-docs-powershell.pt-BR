---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: 3aa6c569eb7f67b6021f7f40059cc9e528355a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888026"
---
# <span data-ttu-id="5b724-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5b724-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="5b724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b724-102">SYNOPSIS</span></span>
<span data-ttu-id="5b724-103">Este comando lista todos os serviços de sincronização de armazenamento dentro de um determinado escopo de grupo de assinatura/recurso.</span><span class="sxs-lookup"><span data-stu-id="5b724-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="5b724-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5b724-104">SYNTAX</span></span>

### <span data-ttu-id="5b724-105">ParentStringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5b724-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b724-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b724-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b724-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5b724-107">DESCRIPTION</span></span>
<span data-ttu-id="5b724-108">Este comando lista todos os serviços de sincronização de armazenamento dentro de um determinado escopo de grupo de assinatura/recurso.</span><span class="sxs-lookup"><span data-stu-id="5b724-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="5b724-109">Ele também pode ser usado para listar os atributos de cada serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5b724-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="5b724-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b724-110">EXAMPLES</span></span>

### <span data-ttu-id="5b724-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b724-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="5b724-112">Este comando lista todos os recursos do serviço de sincronização de armazenamento em um determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b724-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="5b724-113">Ele também pode ser usado para listar os atributos de cada serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5b724-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="5b724-114">Especifique -StorageSyncServiceName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="5b724-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="5b724-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5b724-115">PARAMETERS</span></span>

### <span data-ttu-id="5b724-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b724-116">-DefaultProfile</span></span>
<span data-ttu-id="5b724-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b724-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b724-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5b724-118">-Name</span></span>
<span data-ttu-id="5b724-119">Nome do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5b724-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b724-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b724-120">-ResourceGroupName</span></span>
<span data-ttu-id="5b724-121">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="5b724-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="5b724-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b724-122">CommonParameters</span></span>
<span data-ttu-id="5b724-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b724-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b724-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b724-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b724-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b724-125">INPUTS</span></span>

### <span data-ttu-id="5b724-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5b724-126">System.String</span></span>

## <span data-ttu-id="5b724-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5b724-127">OUTPUTS</span></span>

### <span data-ttu-id="5b724-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="5b724-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="5b724-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="5b724-129">NOTES</span></span>

## <span data-ttu-id="5b724-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b724-130">RELATED LINKS</span></span>
