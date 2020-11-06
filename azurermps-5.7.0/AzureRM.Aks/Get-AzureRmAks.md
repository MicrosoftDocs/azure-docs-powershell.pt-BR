---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: ee8420a8869e1056dc0ee3d942b811c3f70d545d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432137"
---
# <span data-ttu-id="0dc7d-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="0dc7d-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="0dc7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0dc7d-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc7d-103">Liste os clusters gerenciados do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="0dc7d-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dc7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dc7d-104">SYNTAX</span></span>

### <span data-ttu-id="0dc7d-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0dc7d-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc7d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc7d-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0dc7d-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0dc7d-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0dc7d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0dc7d-108">DESCRIPTION</span></span>
<span data-ttu-id="0dc7d-109">Liste os clusters gerenciados do kubernetes.</span><span class="sxs-lookup"><span data-stu-id="0dc7d-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="0dc7d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0dc7d-110">EXAMPLES</span></span>

### <span data-ttu-id="0dc7d-111">Listar todos os clusters do kubernetes</span><span class="sxs-lookup"><span data-stu-id="0dc7d-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="0dc7d-112">OS</span><span class="sxs-lookup"><span data-stu-id="0dc7d-112">PARAMETERS</span></span>

### <span data-ttu-id="0dc7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc7d-113">-DefaultProfile</span></span>
<span data-ttu-id="0dc7d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0dc7d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc7d-115">-ID</span><span class="sxs-lookup"><span data-stu-id="0dc7d-115">-Id</span></span>
<span data-ttu-id="0dc7d-116">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="0dc7d-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc7d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0dc7d-117">-Name</span></span>
<span data-ttu-id="0dc7d-118">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="0dc7d-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc7d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc7d-119">-ResourceGroupName</span></span>
<span data-ttu-id="0dc7d-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0dc7d-120">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc7d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc7d-121">CommonParameters</span></span>
<span data-ttu-id="0dc7d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc7d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc7d-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc7d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc7d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0dc7d-124">INPUTS</span></span>

### <span data-ttu-id="0dc7d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0dc7d-125">System.String</span></span>

## <span data-ttu-id="0dc7d-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0dc7d-126">OUTPUTS</span></span>

### <span data-ttu-id="0dc7d-127">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="0dc7d-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="0dc7d-128">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster, Microsoft. Azure. Commands. AKs, Version = 0.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0dc7d-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster, Microsoft.Azure.Commands.Aks, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0dc7d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0dc7d-129">NOTES</span></span>

## <span data-ttu-id="0dc7d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0dc7d-130">RELATED LINKS</span></span>