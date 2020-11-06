---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 772f0a3bb1198bf5c8d00ad8c0dd708c37c92366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602472"
---
# <span data-ttu-id="372c3-101">Get-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="372c3-101">Get-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="372c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="372c3-102">SYNOPSIS</span></span>
<span data-ttu-id="372c3-103">Obtém um prefixo de IP público</span><span class="sxs-lookup"><span data-stu-id="372c3-103">Gets a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="372c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="372c3-104">SYNTAX</span></span>

### <span data-ttu-id="372c3-105">Assume</span><span class="sxs-lookup"><span data-stu-id="372c3-105">(Default)</span></span>
```
Get-AzureRmPublicIpPrefix [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="372c3-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="372c3-106">GetByNameParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="372c3-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="372c3-107">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmPublicIpPrefix -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="372c3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="372c3-108">DESCRIPTION</span></span>
<span data-ttu-id="372c3-109">O cmdlet **Get-AzureRmPublicIpPrefix** Obtém um ou mais prefixos IP públicos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="372c3-109">The **Get-AzureRmPublicIpPrefix** cmdlet gets one or more public IP prefixes in a resource group.</span></span>

## <span data-ttu-id="372c3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="372c3-110">EXAMPLES</span></span>

### <span data-ttu-id="372c3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="372c3-111">Example 1</span></span>
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -ResourceGroupName $rgname -Name $prefixName
```

<span data-ttu-id="372c3-112">Este comando obtém um recurso de prefixo de IP público com $prefixName no grupo de recursos $rgName</span><span class="sxs-lookup"><span data-stu-id="372c3-112">This command gets a public IP prefix resource with $prefixName in resource group $rgName</span></span>

## <span data-ttu-id="372c3-113">OS</span><span class="sxs-lookup"><span data-stu-id="372c3-113">PARAMETERS</span></span>

### <span data-ttu-id="372c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372c3-114">-DefaultProfile</span></span>
<span data-ttu-id="372c3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="372c3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="372c3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="372c3-116">-Name</span></span>
<span data-ttu-id="372c3-117">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="372c3-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372c3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372c3-118">-ResourceGroupName</span></span>
<span data-ttu-id="372c3-119">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="372c3-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372c3-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="372c3-120">-ResourceId</span></span>
<span data-ttu-id="372c3-121">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="372c3-121">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="372c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372c3-122">CommonParameters</span></span>
<span data-ttu-id="372c3-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="372c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="372c3-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="372c3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372c3-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="372c3-125">INPUTS</span></span>

### <span data-ttu-id="372c3-126">System. String</span><span class="sxs-lookup"><span data-stu-id="372c3-126">System.String</span></span>


## <span data-ttu-id="372c3-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="372c3-127">OUTPUTS</span></span>

### <span data-ttu-id="372c3-128">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="372c3-128">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="372c3-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="372c3-129">NOTES</span></span>

## <span data-ttu-id="372c3-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="372c3-130">RELATED LINKS</span></span>
