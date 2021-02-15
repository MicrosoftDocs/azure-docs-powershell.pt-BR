---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 5b2d10f3ffa2d00942b8198c598c9ec821dead99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112754"
---
# <span data-ttu-id="11d25-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="11d25-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="11d25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11d25-102">SYNOPSIS</span></span>
<span data-ttu-id="11d25-103">Atualiza uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="11d25-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="11d25-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11d25-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11d25-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="11d25-105">DESCRIPTION</span></span>
<span data-ttu-id="11d25-106">O **cmdlet Set-AzServiceEndpointPolicy** cria uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="11d25-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="11d25-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="11d25-107">EXAMPLES</span></span>

### <span data-ttu-id="11d25-108">Exemplo 1: define uma política de ponto de extremidade de serviço</span><span class="sxs-lookup"><span data-stu-id="11d25-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="11d25-109">Esse comando atualiza uma política de ponto de extremidade de serviço chamada Política1 definida pelo objeto $serviceEndpointPolicy pertence ao grupo de recursos "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="11d25-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="11d25-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11d25-110">PARAMETERS</span></span>

### <span data-ttu-id="11d25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d25-111">-DefaultProfile</span></span>
<span data-ttu-id="11d25-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="11d25-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11d25-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="11d25-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="11d25-114">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="11d25-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11d25-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="11d25-115">-Confirm</span></span>
<span data-ttu-id="11d25-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11d25-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d25-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d25-117">-WhatIf</span></span>
<span data-ttu-id="11d25-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="11d25-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11d25-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11d25-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d25-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d25-120">CommonParameters</span></span>
<span data-ttu-id="11d25-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11d25-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d25-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11d25-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d25-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="11d25-123">INPUTS</span></span>

### <span data-ttu-id="11d25-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="11d25-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="11d25-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="11d25-125">OUTPUTS</span></span>

### <span data-ttu-id="11d25-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="11d25-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="11d25-127">Notas</span><span class="sxs-lookup"><span data-stu-id="11d25-127">NOTES</span></span>

## <span data-ttu-id="11d25-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11d25-128">RELATED LINKS</span></span>

[<span data-ttu-id="11d25-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="11d25-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="11d25-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="11d25-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="11d25-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="11d25-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
