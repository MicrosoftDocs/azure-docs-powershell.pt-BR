---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: 52b6a4b7c5f78359ffc046953101aaa01bb7a435
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890797"
---
# <span data-ttu-id="064b9-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="064b9-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="064b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="064b9-102">SYNOPSIS</span></span>
<span data-ttu-id="064b9-103">Obtém um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="064b9-103">Gets an application security group.</span></span>

## <span data-ttu-id="064b9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="064b9-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="064b9-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="064b9-105">DESCRIPTION</span></span>
<span data-ttu-id="064b9-106">O cmdlet **Get-AzApplicationSecurityGroup** obtém um grupo de segurança de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="064b9-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="064b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="064b9-107">EXAMPLES</span></span>

### <span data-ttu-id="064b9-108">Exemplo 1: Recuperar todos os grupos de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="064b9-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="064b9-109">O comando acima retorna todos os grupos de segurança do aplicativo na assinatura.</span><span class="sxs-lookup"><span data-stu-id="064b9-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="064b9-110">Exemplo 2: Recuperar grupos de segurança de aplicativos em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="064b9-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="064b9-111">O comando acima retorna todos os grupos de segurança de aplicativos que pertencem ao grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="064b9-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="064b9-112">Exemplo 3: Recuperar um grupo de segurança de aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="064b9-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="064b9-113">O comando acima retorna o grupo de segurança do aplicativo MyApplicationSecurityGroup no grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="064b9-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="064b9-114">Exemplo 4: Recuperar grupos de segurança de aplicativos usando filtragem.</span><span class="sxs-lookup"><span data-stu-id="064b9-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="064b9-115">O comando acima retorna todos os grupos de segurança de aplicativos que começam com "MyApplicationSecurityGroup".</span><span class="sxs-lookup"><span data-stu-id="064b9-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="064b9-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="064b9-116">PARAMETERS</span></span>

### <span data-ttu-id="064b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="064b9-117">-DefaultProfile</span></span>
<span data-ttu-id="064b9-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="064b9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="064b9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="064b9-119">-Name</span></span>
<span data-ttu-id="064b9-120">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="064b9-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="064b9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="064b9-121">-ResourceGroupName</span></span>
<span data-ttu-id="064b9-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="064b9-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="064b9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="064b9-123">CommonParameters</span></span>
<span data-ttu-id="064b9-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="064b9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="064b9-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="064b9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="064b9-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="064b9-126">INPUTS</span></span>

### <span data-ttu-id="064b9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="064b9-127">System.String</span></span>

## <span data-ttu-id="064b9-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="064b9-128">OUTPUTS</span></span>

### <span data-ttu-id="064b9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="064b9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="064b9-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="064b9-130">NOTES</span></span>

## <span data-ttu-id="064b9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="064b9-131">RELATED LINKS</span></span>

[<span data-ttu-id="064b9-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="064b9-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="064b9-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="064b9-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="064b9-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="064b9-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="064b9-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="064b9-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)
