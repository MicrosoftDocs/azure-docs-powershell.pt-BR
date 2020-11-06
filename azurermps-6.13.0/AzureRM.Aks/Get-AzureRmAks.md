---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: d30d9858a3050864f5cc86601adf6b598be8c54d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432835"
---
# <span data-ttu-id="8e4af-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="8e4af-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="8e4af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e4af-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4af-103">Liste os clusters gerenciados do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8e4af-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e4af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e4af-104">SYNTAX</span></span>

### <span data-ttu-id="8e4af-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e4af-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e4af-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e4af-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e4af-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e4af-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e4af-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e4af-108">DESCRIPTION</span></span>
<span data-ttu-id="8e4af-109">Liste os clusters gerenciados do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="8e4af-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="8e4af-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e4af-110">EXAMPLES</span></span>

### <span data-ttu-id="8e4af-111">Listar todos os clusters do kubernetes</span><span class="sxs-lookup"><span data-stu-id="8e4af-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="8e4af-112">OS</span><span class="sxs-lookup"><span data-stu-id="8e4af-112">PARAMETERS</span></span>

### <span data-ttu-id="8e4af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e4af-113">-DefaultProfile</span></span>
<span data-ttu-id="8e4af-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e4af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4af-115">-ID</span><span class="sxs-lookup"><span data-stu-id="8e4af-115">-Id</span></span>
<span data-ttu-id="8e4af-116">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="8e4af-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e4af-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e4af-117">-Name</span></span>
<span data-ttu-id="8e4af-118">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="8e4af-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e4af-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e4af-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8e4af-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4af-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4af-121">CommonParameters</span></span>
<span data-ttu-id="8e4af-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e4af-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4af-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e4af-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4af-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e4af-124">INPUTS</span></span>

### <span data-ttu-id="8e4af-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8e4af-125">System.String</span></span>

## <span data-ttu-id="8e4af-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e4af-126">OUTPUTS</span></span>

### <span data-ttu-id="8e4af-127">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="8e4af-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="8e4af-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e4af-128">NOTES</span></span>

## <span data-ttu-id="8e4af-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e4af-129">RELATED LINKS</span></span>
