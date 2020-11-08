---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111828"
---
# <span data-ttu-id="b00f4-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b00f4-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="b00f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b00f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b00f4-103">Remove uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b00f4-103">Removes an integration account.</span></span>

## <span data-ttu-id="b00f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b00f4-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b00f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b00f4-105">DESCRIPTION</span></span>
<span data-ttu-id="b00f4-106">O cmdlet **Remove-AzIntegrationAccount** remove uma conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b00f4-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="b00f4-107">Especifique o nome da conta de integração e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b00f4-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="b00f4-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="b00f4-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b00f4-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="b00f4-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b00f4-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b00f4-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b00f4-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="b00f4-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b00f4-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b00f4-112">EXAMPLES</span></span>

### <span data-ttu-id="b00f4-113">Exemplo 1: remover uma conta de integração</span><span class="sxs-lookup"><span data-stu-id="b00f4-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="b00f4-114">Esse comando Remove uma conta de integração chamada IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="b00f4-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="b00f4-115">OS</span><span class="sxs-lookup"><span data-stu-id="b00f4-115">PARAMETERS</span></span>

### <span data-ttu-id="b00f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00f4-116">-DefaultProfile</span></span>
<span data-ttu-id="b00f4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b00f4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b00f4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b00f4-118">-Force</span></span>
<span data-ttu-id="b00f4-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b00f4-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b00f4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b00f4-120">-Name</span></span>
<span data-ttu-id="b00f4-121">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b00f4-121">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="b00f4-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b00f4-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b00f4-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b00f4-124">-Confirm</span></span>
<span data-ttu-id="b00f4-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b00f4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00f4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00f4-126">-WhatIf</span></span>
<span data-ttu-id="b00f4-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b00f4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00f4-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b00f4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00f4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00f4-129">CommonParameters</span></span>
<span data-ttu-id="b00f4-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00f4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00f4-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00f4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00f4-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b00f4-132">INPUTS</span></span>

### <span data-ttu-id="b00f4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b00f4-133">System.String</span></span>

## <span data-ttu-id="b00f4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b00f4-134">OUTPUTS</span></span>

### <span data-ttu-id="b00f4-135">System. void</span><span class="sxs-lookup"><span data-stu-id="b00f4-135">System.Void</span></span>

## <span data-ttu-id="b00f4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b00f4-136">NOTES</span></span>

## <span data-ttu-id="b00f4-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b00f4-137">RELATED LINKS</span></span>

[<span data-ttu-id="b00f4-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b00f4-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="b00f4-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b00f4-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="b00f4-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="b00f4-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


