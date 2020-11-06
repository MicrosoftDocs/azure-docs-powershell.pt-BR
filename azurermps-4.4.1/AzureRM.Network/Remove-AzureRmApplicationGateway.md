---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: cd4824b73aa7fe7a80a3c4bccba37445a85c2c22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427845"
---
# <span data-ttu-id="2efb6-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2efb6-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="2efb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2efb6-102">SYNOPSIS</span></span>
<span data-ttu-id="2efb6-103">Remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2efb6-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2efb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2efb6-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2efb6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2efb6-105">DESCRIPTION</span></span>
<span data-ttu-id="2efb6-106">O cmdlet **Remove-AzureRmApplicationGateway** remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2efb6-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="2efb6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2efb6-107">EXAMPLES</span></span>

### <span data-ttu-id="2efb6-108">Exemplo 1: remover um gateway de aplicativo especificado</span><span class="sxs-lookup"><span data-stu-id="2efb6-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2efb6-109">Esse comando Remove o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2efb6-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="2efb6-110">OS</span><span class="sxs-lookup"><span data-stu-id="2efb6-110">PARAMETERS</span></span>

### <span data-ttu-id="2efb6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2efb6-111">-Force</span></span>
<span data-ttu-id="2efb6-112">Indica que o cmdlet força a exclusão do Application Gateway independentemente de os recursos serem atribuídos a ele.</span><span class="sxs-lookup"><span data-stu-id="2efb6-112">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2efb6-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2efb6-113">-Name</span></span>
<span data-ttu-id="2efb6-114">Especifica o nome do gateway do aplicativo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="2efb6-114">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2efb6-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2efb6-115">-PassThru</span></span>
<span data-ttu-id="2efb6-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="2efb6-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2efb6-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="2efb6-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2efb6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2efb6-118">-ResourceGroupName</span></span>
<span data-ttu-id="2efb6-119">Especifica o nome do grupo de recursos ao qual o gateway do aplicativo pertence.</span><span class="sxs-lookup"><span data-stu-id="2efb6-119">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="2efb6-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2efb6-120">-Confirm</span></span>
<span data-ttu-id="2efb6-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2efb6-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2efb6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2efb6-122">-WhatIf</span></span>
<span data-ttu-id="2efb6-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2efb6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2efb6-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2efb6-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2efb6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2efb6-125">-DefaultProfile</span></span>
<span data-ttu-id="2efb6-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2efb6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2efb6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2efb6-127">CommonParameters</span></span>
<span data-ttu-id="2efb6-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2efb6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2efb6-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2efb6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2efb6-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2efb6-130">INPUTS</span></span>

## <span data-ttu-id="2efb6-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2efb6-131">OUTPUTS</span></span>

### <span data-ttu-id="2efb6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2efb6-132">System.String</span></span>

## <span data-ttu-id="2efb6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2efb6-133">NOTES</span></span>

## <span data-ttu-id="2efb6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2efb6-134">RELATED LINKS</span></span>

[<span data-ttu-id="2efb6-135">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2efb6-135">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


