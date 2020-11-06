---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 49c7a9a28da7822423e43ee655b1ff2256e957e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609388"
---
# <span data-ttu-id="27ea8-101">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27ea8-101">Get-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="27ea8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="27ea8-103">Obtém um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27ea8-103">Gets an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27ea8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27ea8-104">SYNTAX</span></span>

```
Get-AzureRmApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27ea8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="27ea8-106">O cmdlet **Get-AzureRmApplicationSecurityGroup** Obtém um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27ea8-106">The **Get-AzureRmApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="27ea8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27ea8-107">EXAMPLES</span></span>

### <span data-ttu-id="27ea8-108">Exemplo 1: recuperar todos os grupos de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27ea8-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup
```

<span data-ttu-id="27ea8-109">O comando acima retorna todos os grupos de segurança do aplicativo na assinatura.</span><span class="sxs-lookup"><span data-stu-id="27ea8-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="27ea8-110">Exemplo 2: recuperar grupos de segurança do aplicativo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27ea8-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="27ea8-111">O comando acima retorna todos os grupos de segurança do aplicativo que pertencem ao grupo MyResource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27ea8-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="27ea8-112">Exemplo 3: recuperar um grupo de segurança de aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="27ea8-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="27ea8-113">O comando acima retorna o grupo de segurança do aplicativo MyApplicationSecurityGroup sob o grupo MyResource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27ea8-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="27ea8-114">OS</span><span class="sxs-lookup"><span data-stu-id="27ea8-114">PARAMETERS</span></span>

### <span data-ttu-id="27ea8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ea8-115">-DefaultProfile</span></span>
<span data-ttu-id="27ea8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27ea8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27ea8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="27ea8-117">-Name</span></span>
<span data-ttu-id="27ea8-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="27ea8-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ea8-119">-ResourceGroupName</span></span>
<span data-ttu-id="27ea8-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27ea8-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27ea8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ea8-121">CommonParameters</span></span>
<span data-ttu-id="27ea8-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27ea8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ea8-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ea8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ea8-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27ea8-124">INPUTS</span></span>

### <span data-ttu-id="27ea8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="27ea8-125">System.String</span></span>

## <span data-ttu-id="27ea8-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27ea8-126">OUTPUTS</span></span>

### <span data-ttu-id="27ea8-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27ea8-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="27ea8-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27ea8-128">NOTES</span></span>

## <span data-ttu-id="27ea8-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27ea8-129">RELATED LINKS</span></span>

[<span data-ttu-id="27ea8-130">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27ea8-130">New-AzureRmApplicationSecurityGroup</span></span>](./New-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="27ea8-131">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27ea8-131">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="27ea8-132">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27ea8-132">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="27ea8-133">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="27ea8-133">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)
