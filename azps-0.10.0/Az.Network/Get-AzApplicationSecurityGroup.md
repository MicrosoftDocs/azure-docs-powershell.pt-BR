---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: b23901a79262f4eb63e34b99c10b82442cb2fe6a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775565"
---
# <span data-ttu-id="7fe22-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7fe22-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="7fe22-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fe22-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe22-103">Obtém um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fe22-103">Gets an application security group.</span></span>

## <span data-ttu-id="7fe22-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fe22-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fe22-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fe22-105">DESCRIPTION</span></span>
<span data-ttu-id="7fe22-106">O cmdlet **Get-AzApplicationSecurityGroup** Obtém um grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fe22-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="7fe22-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fe22-107">EXAMPLES</span></span>

### <span data-ttu-id="7fe22-108">Exemplo 1: recuperar todos os grupos de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7fe22-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup
```

<span data-ttu-id="7fe22-109">O comando acima retorna todos os grupos de segurança do aplicativo na assinatura.</span><span class="sxs-lookup"><span data-stu-id="7fe22-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="7fe22-110">Exemplo 2: recuperar grupos de segurança do aplicativo em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fe22-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="7fe22-111">O comando acima retorna todos os grupos de segurança do aplicativo que pertencem ao grupo MyResource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fe22-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7fe22-112">Exemplo 3: recuperar um grupo de segurança de aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="7fe22-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup
```

<span data-ttu-id="7fe22-113">O comando acima retorna o grupo de segurança do aplicativo MyApplicationSecurityGroup sob o grupo MyResource do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fe22-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

## <span data-ttu-id="7fe22-114">OS</span><span class="sxs-lookup"><span data-stu-id="7fe22-114">PARAMETERS</span></span>

### <span data-ttu-id="7fe22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe22-115">-DefaultProfile</span></span>
<span data-ttu-id="7fe22-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe22-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fe22-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7fe22-117">-Name</span></span>
<span data-ttu-id="7fe22-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7fe22-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe22-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fe22-119">-ResourceGroupName</span></span>
<span data-ttu-id="7fe22-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fe22-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe22-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe22-121">CommonParameters</span></span>
<span data-ttu-id="7fe22-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fe22-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe22-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fe22-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe22-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fe22-124">INPUTS</span></span>

### <span data-ttu-id="7fe22-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7fe22-125">System.String</span></span>

## <span data-ttu-id="7fe22-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fe22-126">OUTPUTS</span></span>

### <span data-ttu-id="7fe22-127">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7fe22-127">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="7fe22-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fe22-128">NOTES</span></span>

## <span data-ttu-id="7fe22-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fe22-129">RELATED LINKS</span></span>

[<span data-ttu-id="7fe22-130">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7fe22-130">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="7fe22-131">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="7fe22-131">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="7fe22-132">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7fe22-132">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="7fe22-133">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7fe22-133">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
