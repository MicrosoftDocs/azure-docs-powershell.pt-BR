---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263585"
---
# <span data-ttu-id="75478-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="75478-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="75478-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="75478-102">SYNOPSIS</span></span>
<span data-ttu-id="75478-103">Esse comando lista todos os serviços de sincronização de armazenamento em um determinado escopo de grupo de assinaturas/recursos.</span><span class="sxs-lookup"><span data-stu-id="75478-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="75478-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="75478-104">SYNTAX</span></span>

### <span data-ttu-id="75478-105">ParentStringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="75478-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="75478-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="75478-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75478-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="75478-107">DESCRIPTION</span></span>
<span data-ttu-id="75478-108">Esse comando lista todos os serviços de sincronização de armazenamento em um determinado escopo de grupo de assinaturas/recursos.</span><span class="sxs-lookup"><span data-stu-id="75478-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="75478-109">Ele também pode ser usado para listar os atributos de cada serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="75478-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="75478-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75478-110">EXAMPLES</span></span>

### <span data-ttu-id="75478-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="75478-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="75478-112">Esse comando lista todos os recursos do serviço de sincronização de armazenamento em um determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75478-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="75478-113">Ele também pode ser usado para listar os atributos de cada serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="75478-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="75478-114">Especifique-StorageSyncServiceName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="75478-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="75478-115">OS</span><span class="sxs-lookup"><span data-stu-id="75478-115">PARAMETERS</span></span>

### <span data-ttu-id="75478-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75478-116">-DefaultProfile</span></span>
<span data-ttu-id="75478-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="75478-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75478-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="75478-118">-Name</span></span>
<span data-ttu-id="75478-119">Nome do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="75478-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="75478-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75478-120">-ResourceGroupName</span></span>
<span data-ttu-id="75478-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75478-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="75478-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75478-122">CommonParameters</span></span>
<span data-ttu-id="75478-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75478-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75478-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75478-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75478-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="75478-125">INPUTS</span></span>

### <span data-ttu-id="75478-126">System. String</span><span class="sxs-lookup"><span data-stu-id="75478-126">System.String</span></span>

## <span data-ttu-id="75478-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="75478-127">OUTPUTS</span></span>

### <span data-ttu-id="75478-128">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="75478-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="75478-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="75478-129">NOTES</span></span>

## <span data-ttu-id="75478-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75478-130">RELATED LINKS</span></span>
