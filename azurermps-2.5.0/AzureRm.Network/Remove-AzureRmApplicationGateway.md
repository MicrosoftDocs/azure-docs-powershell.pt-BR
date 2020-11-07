---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 99ac8e367c42cd59b3f055aa4a86a3efd4f297a0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785667"
---
# <span data-ttu-id="08a0b-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08a0b-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="08a0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="08a0b-103">Remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="08a0b-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08a0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08a0b-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08a0b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="08a0b-106">O cmdlet **Remove-AzureRmApplicationGateway** remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="08a0b-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="08a0b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08a0b-107">EXAMPLES</span></span>

### <span data-ttu-id="08a0b-108">Exemplo 1: remover um gateway de aplicativo especificado</span><span class="sxs-lookup"><span data-stu-id="08a0b-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="08a0b-109">Esse comando Remove o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="08a0b-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="08a0b-110">OS</span><span class="sxs-lookup"><span data-stu-id="08a0b-110">PARAMETERS</span></span>

### <span data-ttu-id="08a0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08a0b-111">-DefaultProfile</span></span>
<span data-ttu-id="08a0b-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08a0b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08a0b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="08a0b-113">-Force</span></span>
<span data-ttu-id="08a0b-114">Indica que o cmdlet força a exclusão do Application Gateway independentemente de os recursos serem atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="08a0b-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08a0b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="08a0b-115">-Name</span></span>
<span data-ttu-id="08a0b-116">Especifica o nome do gateway do aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="08a0b-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08a0b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08a0b-117">-PassThru</span></span>
<span data-ttu-id="08a0b-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="08a0b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="08a0b-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="08a0b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08a0b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08a0b-120">-ResourceGroupName</span></span>
<span data-ttu-id="08a0b-121">Especifica o nome do grupo de recursos ao qual o gateway do aplicativo pertence.</span><span class="sxs-lookup"><span data-stu-id="08a0b-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="08a0b-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="08a0b-122">-Confirm</span></span>
<span data-ttu-id="08a0b-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08a0b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a0b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08a0b-124">-WhatIf</span></span>
<span data-ttu-id="08a0b-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08a0b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08a0b-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08a0b-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08a0b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08a0b-127">CommonParameters</span></span>
<span data-ttu-id="08a0b-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08a0b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08a0b-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08a0b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08a0b-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08a0b-130">INPUTS</span></span>

## <span data-ttu-id="08a0b-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08a0b-131">OUTPUTS</span></span>

### <span data-ttu-id="08a0b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="08a0b-132">System.String</span></span>

## <span data-ttu-id="08a0b-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08a0b-133">NOTES</span></span>

## <span data-ttu-id="08a0b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08a0b-134">RELATED LINKS</span></span>

[<span data-ttu-id="08a0b-135">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08a0b-135">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


