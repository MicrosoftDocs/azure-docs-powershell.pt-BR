---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 46515fc76d246ffdb4207afb0300613b52cae0a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610314"
---
# <span data-ttu-id="0a281-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a281-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="0a281-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a281-102">SYNOPSIS</span></span>
<span data-ttu-id="0a281-103">Remove um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a281-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a281-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a281-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a281-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a281-105">DESCRIPTION</span></span>
<span data-ttu-id="0a281-106">O cmdlet **Remove-AzureRmLogicApp** remove um aplicativo lógico de um grupo de recursos usando o recurso de aplicativos lógicos.</span><span class="sxs-lookup"><span data-stu-id="0a281-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="0a281-107">Especifique o aplicativo lógico e o grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a281-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="0a281-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="0a281-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0a281-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="0a281-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0a281-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0a281-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0a281-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="0a281-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0a281-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a281-112">EXAMPLES</span></span>

### <span data-ttu-id="0a281-113">Exemplo 1: remover um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="0a281-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="0a281-114">Esse comando Remove um aplicativo lógico de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0a281-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="0a281-115">O comando inclui o parâmetro *Force* , que impede que o comando solicite confirmação.</span><span class="sxs-lookup"><span data-stu-id="0a281-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="0a281-116">OS</span><span class="sxs-lookup"><span data-stu-id="0a281-116">PARAMETERS</span></span>

### <span data-ttu-id="0a281-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a281-117">-DefaultProfile</span></span>
<span data-ttu-id="0a281-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0a281-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a281-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0a281-119">-Force</span></span>
<span data-ttu-id="0a281-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0a281-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0a281-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a281-121">-Name</span></span>
<span data-ttu-id="0a281-122">Especifica o nome do aplicativo lógico que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0a281-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a281-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a281-123">-ResourceGroupName</span></span>
<span data-ttu-id="0a281-124">Especifica o nome do grupo de recursos que contém o aplicativo lógico que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="0a281-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0a281-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a281-125">-Confirm</span></span>
<span data-ttu-id="0a281-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a281-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a281-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a281-127">-WhatIf</span></span>
<span data-ttu-id="0a281-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a281-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a281-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a281-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a281-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a281-130">CommonParameters</span></span>
<span data-ttu-id="0a281-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a281-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a281-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a281-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a281-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a281-133">INPUTS</span></span>

### <span data-ttu-id="0a281-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0a281-134">System.String</span></span>

## <span data-ttu-id="0a281-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a281-135">OUTPUTS</span></span>

### <span data-ttu-id="0a281-136">System. void</span><span class="sxs-lookup"><span data-stu-id="0a281-136">System.Void</span></span>

## <span data-ttu-id="0a281-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a281-137">NOTES</span></span>

## <span data-ttu-id="0a281-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a281-138">RELATED LINKS</span></span>

[<span data-ttu-id="0a281-139">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a281-139">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="0a281-140">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a281-140">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="0a281-141">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a281-141">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="0a281-142">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="0a281-142">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


