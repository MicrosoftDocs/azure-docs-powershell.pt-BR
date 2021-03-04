---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: b5f555a0df848c86dbbc0a04297d45b4132e6972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885610"
---
# <span data-ttu-id="08fa3-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="08fa3-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="08fa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="08fa3-103">Cria uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="08fa3-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="08fa3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="08fa3-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08fa3-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="08fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="08fa3-106">O cmdlet **New-AzServiceEndpointPolicy** cria uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="08fa3-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="08fa3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08fa3-107">EXAMPLES</span></span>

### <span data-ttu-id="08fa3-108">Exemplo 1: cria uma política de ponto de extremidade de serviço</span><span class="sxs-lookup"><span data-stu-id="08fa3-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="08fa3-109">Este comando cria uma política de ponto de extremidade de serviço chamada Policy1 com definições definidas pelo objeto $serviceEndpointDefinition e a armazena na variável $serviceEndpointPolicy de serviço.</span><span class="sxs-lookup"><span data-stu-id="08fa3-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="08fa3-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="08fa3-110">PARAMETERS</span></span>

### <span data-ttu-id="08fa3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08fa3-111">-DefaultProfile</span></span>
<span data-ttu-id="08fa3-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="08fa3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08fa3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="08fa3-113">-Force</span></span>
<span data-ttu-id="08fa3-114">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="08fa3-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-115">-Location</span><span class="sxs-lookup"><span data-stu-id="08fa3-115">-Location</span></span>
<span data-ttu-id="08fa3-116">location.</span><span class="sxs-lookup"><span data-stu-id="08fa3-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-117">-Name</span><span class="sxs-lookup"><span data-stu-id="08fa3-117">-Name</span></span>
<span data-ttu-id="08fa3-118">O nome da sub-rede</span><span class="sxs-lookup"><span data-stu-id="08fa3-118">The name of the subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08fa3-119">-ResourceGroupName</span></span>
<span data-ttu-id="08fa3-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="08fa3-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="08fa3-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="08fa3-122">Lista de definições de ponto de extremidade de serviço</span><span class="sxs-lookup"><span data-stu-id="08fa3-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08fa3-123">-Confirm</span></span>
<span data-ttu-id="08fa3-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08fa3-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08fa3-125">-WhatIf</span></span>
<span data-ttu-id="08fa3-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08fa3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08fa3-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08fa3-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08fa3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08fa3-128">CommonParameters</span></span>
<span data-ttu-id="08fa3-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08fa3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08fa3-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08fa3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08fa3-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08fa3-131">INPUTS</span></span>

### <span data-ttu-id="08fa3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="08fa3-132">System.String</span></span>

## <span data-ttu-id="08fa3-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="08fa3-133">OUTPUTS</span></span>

### <span data-ttu-id="08fa3-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="08fa3-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="08fa3-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="08fa3-135">NOTES</span></span>

## <span data-ttu-id="08fa3-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08fa3-136">RELATED LINKS</span></span>

[<span data-ttu-id="08fa3-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="08fa3-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="08fa3-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="08fa3-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="08fa3-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="08fa3-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
