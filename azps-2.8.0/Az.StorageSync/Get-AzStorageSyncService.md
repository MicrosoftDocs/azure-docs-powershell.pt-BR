---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: 9eca6930caccd2796362e32f1617ee98bcda0885
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774300"
---
# <span data-ttu-id="dd51b-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dd51b-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="dd51b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd51b-102">SYNOPSIS</span></span>
<span data-ttu-id="dd51b-103">Esse comando lista todos os serviços de sincronização de armazenamento em um determinado escopo de grupo de assinaturas/recursos.</span><span class="sxs-lookup"><span data-stu-id="dd51b-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="dd51b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd51b-104">SYNTAX</span></span>

### <span data-ttu-id="dd51b-105">ParentStringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd51b-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd51b-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd51b-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd51b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd51b-107">DESCRIPTION</span></span>
<span data-ttu-id="dd51b-108">Esse comando lista todos os serviços de sincronização de armazenamento em um determinado escopo de grupo de assinaturas/recursos.</span><span class="sxs-lookup"><span data-stu-id="dd51b-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="dd51b-109">Ele também pode ser usado para listar os atributos de cada serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dd51b-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="dd51b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd51b-110">EXAMPLES</span></span>

### <span data-ttu-id="dd51b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd51b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="dd51b-112">Esse comando lista todos os recursos do serviço de sincronização de armazenamento em um determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd51b-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="dd51b-113">Ele também pode ser usado para listar os atributos de cada serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dd51b-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="dd51b-114">Especifique-StorageSyncServiceName para retornar um específico.</span><span class="sxs-lookup"><span data-stu-id="dd51b-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="dd51b-115">OS</span><span class="sxs-lookup"><span data-stu-id="dd51b-115">PARAMETERS</span></span>

### <span data-ttu-id="dd51b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd51b-116">-DefaultProfile</span></span>
<span data-ttu-id="dd51b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd51b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd51b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd51b-118">-Name</span></span>
<span data-ttu-id="dd51b-119">Nome do serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dd51b-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="dd51b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd51b-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd51b-121">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd51b-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd51b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd51b-122">CommonParameters</span></span>
<span data-ttu-id="dd51b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd51b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd51b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd51b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd51b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd51b-125">INPUTS</span></span>

### <span data-ttu-id="dd51b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dd51b-126">System.String</span></span>

## <span data-ttu-id="dd51b-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd51b-127">OUTPUTS</span></span>

### <span data-ttu-id="dd51b-128">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dd51b-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="dd51b-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd51b-129">NOTES</span></span>

## <span data-ttu-id="dd51b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd51b-130">RELATED LINKS</span></span>
