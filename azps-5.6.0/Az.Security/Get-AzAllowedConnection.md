---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 211601ac2866dab85d46e61cba79ed074f79e22d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887634"
---
# <span data-ttu-id="02358-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="02358-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="02358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02358-102">SYNOPSIS</span></span>
<span data-ttu-id="02358-103">Usado para exibir tráfego permitido entre recursos para a assinatura</span><span class="sxs-lookup"><span data-stu-id="02358-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="02358-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="02358-104">SYNTAX</span></span>

### <span data-ttu-id="02358-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="02358-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02358-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="02358-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02358-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02358-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02358-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="02358-108">DESCRIPTION</span></span>
<span data-ttu-id="02358-109">Obtém a lista de todo o tráfego possível entre recursos para a assinatura e o local, com base no tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="02358-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="02358-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02358-110">EXAMPLES</span></span>

### <span data-ttu-id="02358-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02358-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="02358-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="02358-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="02358-113">Obtém a lista de todo o tráfego possível entre recursos para a assinatura e o local, com base no tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="02358-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="02358-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="02358-114">PARAMETERS</span></span>

### <span data-ttu-id="02358-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02358-115">-DefaultProfile</span></span>
<span data-ttu-id="02358-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02358-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02358-117">-Location</span><span class="sxs-lookup"><span data-stu-id="02358-117">-Location</span></span>
<span data-ttu-id="02358-118">Local.</span><span class="sxs-lookup"><span data-stu-id="02358-118">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02358-119">-Name</span><span class="sxs-lookup"><span data-stu-id="02358-119">-Name</span></span>
<span data-ttu-id="02358-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="02358-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02358-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02358-121">-ResourceGroupName</span></span>
<span data-ttu-id="02358-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02358-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02358-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02358-123">-ResourceId</span></span>
<span data-ttu-id="02358-124">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="02358-124">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02358-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02358-125">CommonParameters</span></span>
<span data-ttu-id="02358-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02358-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02358-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02358-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02358-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02358-128">INPUTS</span></span>

### <span data-ttu-id="02358-129">System.String</span><span class="sxs-lookup"><span data-stu-id="02358-129">System.String</span></span>

## <span data-ttu-id="02358-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="02358-130">OUTPUTS</span></span>

### <span data-ttu-id="02358-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="02358-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="02358-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="02358-132">NOTES</span></span>

## <span data-ttu-id="02358-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02358-133">RELATED LINKS</span></span>
