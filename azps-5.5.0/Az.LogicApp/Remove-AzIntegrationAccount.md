---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccount.md
ms.openlocfilehash: 1daffb4bd4c6f78c0022057faa3bef052531dd46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113619"
---
# <span data-ttu-id="10f93-101">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="10f93-101">Remove-AzIntegrationAccount</span></span>

## <span data-ttu-id="10f93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10f93-102">SYNOPSIS</span></span>
<span data-ttu-id="10f93-103">Remove uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="10f93-103">Removes an integration account.</span></span>

## <span data-ttu-id="10f93-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10f93-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10f93-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="10f93-105">DESCRIPTION</span></span>
<span data-ttu-id="10f93-106">O **cmdlet Remove-AzIntegrationAccount** remove uma conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10f93-106">The **Remove-AzIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="10f93-107">Especifique o nome da conta de integração e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10f93-107">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="10f93-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="10f93-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="10f93-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="10f93-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="10f93-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="10f93-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="10f93-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="10f93-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="10f93-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="10f93-112">EXAMPLES</span></span>

### <span data-ttu-id="10f93-113">Exemplo 1: Remover uma conta de integração</span><span class="sxs-lookup"><span data-stu-id="10f93-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="10f93-114">Esse comando remove uma conta de integração chamada IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="10f93-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="10f93-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10f93-115">PARAMETERS</span></span>

### <span data-ttu-id="10f93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f93-116">-DefaultProfile</span></span>
<span data-ttu-id="10f93-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="10f93-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10f93-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="10f93-118">-Force</span></span>
<span data-ttu-id="10f93-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="10f93-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10f93-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="10f93-120">-Name</span></span>
<span data-ttu-id="10f93-121">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="10f93-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="10f93-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10f93-122">-ResourceGroupName</span></span>
<span data-ttu-id="10f93-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="10f93-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="10f93-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="10f93-124">-Confirm</span></span>
<span data-ttu-id="10f93-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10f93-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10f93-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10f93-126">-WhatIf</span></span>
<span data-ttu-id="10f93-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="10f93-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10f93-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10f93-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10f93-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f93-129">CommonParameters</span></span>
<span data-ttu-id="10f93-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f93-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f93-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10f93-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f93-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="10f93-132">INPUTS</span></span>

### <span data-ttu-id="10f93-133">System.String</span><span class="sxs-lookup"><span data-stu-id="10f93-133">System.String</span></span>

## <span data-ttu-id="10f93-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="10f93-134">OUTPUTS</span></span>

### <span data-ttu-id="10f93-135">System.Void</span><span class="sxs-lookup"><span data-stu-id="10f93-135">System.Void</span></span>

## <span data-ttu-id="10f93-136">Notas</span><span class="sxs-lookup"><span data-stu-id="10f93-136">NOTES</span></span>

## <span data-ttu-id="10f93-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10f93-137">RELATED LINKS</span></span>

[<span data-ttu-id="10f93-138">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="10f93-138">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="10f93-139">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="10f93-139">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)

[<span data-ttu-id="10f93-140">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="10f93-140">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)


