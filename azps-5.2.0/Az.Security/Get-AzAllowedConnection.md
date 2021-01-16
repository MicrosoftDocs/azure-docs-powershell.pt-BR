---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzAllowedConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzAllowedConnection.md
ms.openlocfilehash: 3a604cbdda30612016763fef75fcf62e0c8e36f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259453"
---
# <span data-ttu-id="c0398-101">Get-AzAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="c0398-101">Get-AzAllowedConnection</span></span>

## <span data-ttu-id="c0398-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0398-102">SYNOPSIS</span></span>
<span data-ttu-id="c0398-103">Usado para exibir o tráfego permitido entre recursos para a assinatura</span><span class="sxs-lookup"><span data-stu-id="c0398-103">Used to display allowed traffic between resources for the subscription</span></span>


## <span data-ttu-id="c0398-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0398-104">SYNTAX</span></span>

### <span data-ttu-id="c0398-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0398-105">SubscriptionScope (Default)</span></span>
```
Get-AzAllowedConnection [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0398-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="c0398-106">ResourceGroupLevelResource</span></span>
```
Get-AzAllowedConnection -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0398-107">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0398-107">-ResourceId</span></span>
```
Get-AzAllowedConnection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0398-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0398-108">DESCRIPTION</span></span>
<span data-ttu-id="c0398-109">Obtém a lista de todos os possíveis tráfegos entre recursos para a assinatura e o local, com base no tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="c0398-109">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="c0398-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0398-110">EXAMPLES</span></span>

### <span data-ttu-id="c0398-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c0398-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAllowedConnection
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/virtualMachines
Name:   Internal
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

### <span data-ttu-id="c0398-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c0398-112">Example 2</span></span>
```powershell
PS C:\> Get-AzAllowedConnection -ResourceGroupName "myService1" -Location "centralus" -Name "Internal"
Id: /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/allowedConnections/Internal
Name:   virtualMachines
Type:   Microsoft.Security/locations/allowedConnections
CalculatedDateTime: 03-Jun-20 3:03:48 PM
ConnectableResources:   /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myvm
```

<span data-ttu-id="c0398-113">Obtém a lista de todos os possíveis tráfegos entre recursos para a assinatura e o local, com base no tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="c0398-113">Gets the list of all possible traffic between resources for the subscription and location, based on connection type.</span></span>

## <span data-ttu-id="c0398-114">OS</span><span class="sxs-lookup"><span data-stu-id="c0398-114">PARAMETERS</span></span>

### <span data-ttu-id="c0398-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0398-115">-DefaultProfile</span></span>
<span data-ttu-id="c0398-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c0398-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0398-117">-Local</span><span class="sxs-lookup"><span data-stu-id="c0398-117">-Location</span></span>
<span data-ttu-id="c0398-118">Ponto.</span><span class="sxs-lookup"><span data-stu-id="c0398-118">Location.</span></span>

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

### <span data-ttu-id="c0398-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0398-119">-Name</span></span>
<span data-ttu-id="c0398-120">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="c0398-120">Resource name.</span></span>

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

### <span data-ttu-id="c0398-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0398-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0398-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0398-122">Resource group name.</span></span>

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

### <span data-ttu-id="c0398-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0398-123">-ResourceId</span></span>
<span data-ttu-id="c0398-124">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="c0398-124">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="c0398-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0398-125">CommonParameters</span></span>
<span data-ttu-id="c0398-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0398-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0398-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0398-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0398-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0398-128">INPUTS</span></span>

### <span data-ttu-id="c0398-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c0398-129">System.String</span></span>

## <span data-ttu-id="c0398-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0398-130">OUTPUTS</span></span>

### <span data-ttu-id="c0398-131">Microsoft. Azure. Commands. Security. Models. AllowedConnection. PSSecurityAllowedConnection</span><span class="sxs-lookup"><span data-stu-id="c0398-131">Microsoft.Azure.Commands.Security.Models.AllowedConnection.PSSecurityAllowedConnection</span></span>


## <span data-ttu-id="c0398-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0398-132">NOTES</span></span>

## <span data-ttu-id="c0398-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0398-133">RELATED LINKS</span></span>
