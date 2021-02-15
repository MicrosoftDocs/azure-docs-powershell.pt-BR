---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114386"
---
# <span data-ttu-id="2ed14-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2ed14-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="2ed14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ed14-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed14-103">Esse comando lista todos os serviços de sincronização de armazenamento dentro de um determinado escopo de grupo de recursos/assinatura.</span><span class="sxs-lookup"><span data-stu-id="2ed14-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="2ed14-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ed14-104">SYNTAX</span></span>

### <span data-ttu-id="2ed14-105">ParentStringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2ed14-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ed14-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ed14-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ed14-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ed14-107">DESCRIPTION</span></span>
<span data-ttu-id="2ed14-108">Esse comando lista todos os serviços de sincronização de armazenamento dentro de um determinado escopo de grupo de recursos/assinatura.</span><span class="sxs-lookup"><span data-stu-id="2ed14-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="2ed14-109">Ele também pode ser usado para listar os atributos de cada serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2ed14-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="2ed14-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2ed14-110">EXAMPLES</span></span>

### <span data-ttu-id="2ed14-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ed14-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="2ed14-112">Esse comando lista todos os recursos de serviço de sincronização de armazenamento dentro de um determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ed14-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="2ed14-113">Ele também pode ser usado para listar os atributos de cada serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2ed14-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="2ed14-114">Especifique -StorageSyncServiceName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="2ed14-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="2ed14-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ed14-115">PARAMETERS</span></span>

### <span data-ttu-id="2ed14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed14-116">-DefaultProfile</span></span>
<span data-ttu-id="2ed14-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ed14-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ed14-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ed14-118">-Name</span></span>
<span data-ttu-id="2ed14-119">Nome do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2ed14-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="2ed14-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ed14-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ed14-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ed14-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="2ed14-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed14-122">CommonParameters</span></span>
<span data-ttu-id="2ed14-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ed14-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed14-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed14-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed14-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="2ed14-125">INPUTS</span></span>

### <span data-ttu-id="2ed14-126">System.String</span><span class="sxs-lookup"><span data-stu-id="2ed14-126">System.String</span></span>

## <span data-ttu-id="2ed14-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="2ed14-127">OUTPUTS</span></span>

### <span data-ttu-id="2ed14-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2ed14-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="2ed14-129">Notas</span><span class="sxs-lookup"><span data-stu-id="2ed14-129">NOTES</span></span>

## <span data-ttu-id="2ed14-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ed14-130">RELATED LINKS</span></span>
