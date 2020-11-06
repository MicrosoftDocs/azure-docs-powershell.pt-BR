---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 3650e04b8c6d254b396072c55d39cde38a1328f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431652"
---
# <span data-ttu-id="5b11f-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="5b11f-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="5b11f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b11f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b11f-103">Remove um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b11f-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b11f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5b11f-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b11f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5b11f-105">DESCRIPTION</span></span>
<span data-ttu-id="5b11f-106">O cmdlet **Remove-AzureRmLogicApp** remove um aplicativo lógico de um grupo de recursos usando o recurso de aplicativos lógicos.</span><span class="sxs-lookup"><span data-stu-id="5b11f-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="5b11f-107">Especifique o aplicativo lógico e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b11f-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="5b11f-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="5b11f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5b11f-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="5b11f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5b11f-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5b11f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5b11f-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="5b11f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5b11f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b11f-112">EXAMPLES</span></span>

### <span data-ttu-id="5b11f-113">Exemplo 1: remover um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="5b11f-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="5b11f-114">Esse comando Remove um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b11f-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="5b11f-115">O comando inclui o parâmetro *Force* , que impede que o comando solicite confirmação.</span><span class="sxs-lookup"><span data-stu-id="5b11f-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="5b11f-116">OS</span><span class="sxs-lookup"><span data-stu-id="5b11f-116">PARAMETERS</span></span>

### <span data-ttu-id="5b11f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b11f-117">-DefaultProfile</span></span>
<span data-ttu-id="5b11f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5b11f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b11f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5b11f-119">-Force</span></span>
<span data-ttu-id="5b11f-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5b11f-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5b11f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b11f-121">-Name</span></span>
<span data-ttu-id="5b11f-122">Especifica o nome do aplicativo lógico que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5b11f-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b11f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b11f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5b11f-124">Especifica o nome do grupo de recursos que contém o aplicativo lógico que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="5b11f-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5b11f-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5b11f-125">-Confirm</span></span>
<span data-ttu-id="5b11f-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b11f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b11f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b11f-127">-WhatIf</span></span>
<span data-ttu-id="5b11f-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5b11f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b11f-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b11f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b11f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b11f-130">CommonParameters</span></span>
<span data-ttu-id="5b11f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b11f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b11f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b11f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b11f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5b11f-133">INPUTS</span></span>

### <span data-ttu-id="5b11f-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5b11f-134">None</span></span>
<span data-ttu-id="5b11f-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5b11f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b11f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5b11f-136">OUTPUTS</span></span>

### <span data-ttu-id="5b11f-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="5b11f-137">System.Object</span></span>

## <span data-ttu-id="5b11f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5b11f-138">NOTES</span></span>

## <span data-ttu-id="5b11f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b11f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5b11f-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="5b11f-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="5b11f-141">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="5b11f-141">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="5b11f-142">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="5b11f-142">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="5b11f-143">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="5b11f-143">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


