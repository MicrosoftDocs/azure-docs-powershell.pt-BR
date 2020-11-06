---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 657c18a02f05f2e318fe676a672e894a4aec9e50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433203"
---
# <span data-ttu-id="e7c91-101">New-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e7c91-101">New-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="e7c91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7c91-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c91-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="e7c91-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7c91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7c91-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicy -Name <String>
 [-ServiceEndpointDefinitions <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]>]
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7c91-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7c91-105">DESCRIPTION</span></span>
<span data-ttu-id="e7c91-106">O cmdlet **New-AzureRmServiceEndpointPolicy** cria uma política de ponto de extremidade do serviço.</span><span class="sxs-lookup"><span data-stu-id="e7c91-106">The **New-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="e7c91-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7c91-107">EXAMPLES</span></span>

### <span data-ttu-id="e7c91-108">Exemplo 1: cria uma política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="e7c91-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="e7c91-109">Esse comando cria uma política de ponto de extremidade de serviço chamada Policy1 com definições definidas pelo objeto $serviceEndpointDefinition e as armazena na variável $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="e7c91-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="e7c91-110">OS</span><span class="sxs-lookup"><span data-stu-id="e7c91-110">PARAMETERS</span></span>

### <span data-ttu-id="e7c91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c91-111">-DefaultProfile</span></span>
<span data-ttu-id="e7c91-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7c91-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7c91-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e7c91-113">-Force</span></span>
<span data-ttu-id="e7c91-114">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="e7c91-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c91-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7c91-115">-Name</span></span>
<span data-ttu-id="e7c91-116">O nome da sub-rede</span><span class="sxs-lookup"><span data-stu-id="e7c91-116">The name of the subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c91-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7c91-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7c91-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e7c91-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7c91-119">-ServiceEndpointDefinitions</span><span class="sxs-lookup"><span data-stu-id="e7c91-119">-ServiceEndpointDefinitions</span></span>
<span data-ttu-id="e7c91-120">Lista de definições de ponto de extremidade de serviço</span><span class="sxs-lookup"><span data-stu-id="e7c91-120">List of service endpoint definitions</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c91-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7c91-121">-Confirm</span></span>
<span data-ttu-id="e7c91-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7c91-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c91-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7c91-123">-WhatIf</span></span>
<span data-ttu-id="e7c91-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7c91-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7c91-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7c91-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7c91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c91-126">CommonParameters</span></span>
<span data-ttu-id="e7c91-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7c91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e7c91-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7c91-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c91-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7c91-129">INPUTS</span></span>

### <span data-ttu-id="e7c91-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e7c91-130">System.String</span></span>


## <span data-ttu-id="e7c91-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7c91-131">OUTPUTS</span></span>

### <span data-ttu-id="e7c91-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e7c91-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="e7c91-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7c91-133">NOTES</span></span>

## <span data-ttu-id="e7c91-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7c91-134">RELATED LINKS</span></span>
