---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: f3871e23c0d193ef2ea89c43e3a30c5597abbfe0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440336"
---
# <span data-ttu-id="bd790-101">Remove-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="bd790-101">Remove-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="bd790-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd790-102">SYNOPSIS</span></span>
<span data-ttu-id="bd790-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="bd790-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd790-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd790-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd790-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd790-105">DESCRIPTION</span></span>
<span data-ttu-id="bd790-106">O cmdlet **Remove-AzureRmServiceEndpointPolicy** remove uma política de ponto de extremidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="bd790-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="bd790-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd790-107">EXAMPLES</span></span>

### <span data-ttu-id="bd790-108">Exemplo 1: Remove uma política de ponto de extremidade do serviço usando Name</span><span class="sxs-lookup"><span data-stu-id="bd790-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="bd790-109">Esse comando Remove uma política de ponto de extremidade de serviço com o nome Policy1 que pertence a um MySource com o nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="bd790-109">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="bd790-110">Exemplo 2: remover uma política de ponto de extremidade de serviço usando objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="bd790-110">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzureRmServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="bd790-111">Esse comando Remove um objeto de política de ponto de extremidade de serviço de Policy1 que pertence a um nome de resourcegroup1 "</span><span class="sxs-lookup"><span data-stu-id="bd790-111">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="bd790-112">OS</span><span class="sxs-lookup"><span data-stu-id="bd790-112">PARAMETERS</span></span>

### <span data-ttu-id="bd790-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd790-113">-DefaultProfile</span></span>
<span data-ttu-id="bd790-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd790-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd790-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bd790-115">-Force</span></span>
<span data-ttu-id="bd790-116">Não pedir confirmação se quiser sobreformular um recurso</span><span class="sxs-lookup"><span data-stu-id="bd790-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="bd790-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd790-117">-Name</span></span>
<span data-ttu-id="bd790-118">O nome da política de ponto de extremidade do serviço</span><span class="sxs-lookup"><span data-stu-id="bd790-118">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="bd790-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd790-119">-PassThru</span></span>
<span data-ttu-id="bd790-120">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="bd790-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bd790-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd790-121">-ResourceGroupName</span></span>
<span data-ttu-id="bd790-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd790-122">The resource group name.</span></span>

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

### <span data-ttu-id="bd790-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bd790-123">-Confirm</span></span>
<span data-ttu-id="bd790-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd790-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd790-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd790-125">-WhatIf</span></span>
<span data-ttu-id="bd790-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bd790-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd790-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bd790-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd790-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd790-128">CommonParameters</span></span>
<span data-ttu-id="bd790-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd790-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bd790-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd790-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd790-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd790-131">INPUTS</span></span>

### <span data-ttu-id="bd790-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bd790-132">System.String</span></span>


## <span data-ttu-id="bd790-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd790-133">OUTPUTS</span></span>

### <span data-ttu-id="bd790-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="bd790-134">System.Object</span></span>

## <span data-ttu-id="bd790-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd790-135">NOTES</span></span>

## <span data-ttu-id="bd790-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd790-136">RELATED LINKS</span></span>
