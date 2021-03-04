---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: b66c14eced87cb56b5e8b57766b268a63dbdb088
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886625"
---
# <span data-ttu-id="c9958-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="c9958-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="c9958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9958-102">SYNOPSIS</span></span>
<span data-ttu-id="c9958-103">Remove um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c9958-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="c9958-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c9958-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9958-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c9958-105">DESCRIPTION</span></span>
<span data-ttu-id="c9958-106">O cmdlet **Remove-AzIntegrationAccountSchema** remove um esquema de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9958-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="c9958-107">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="c9958-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="c9958-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="c9958-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c9958-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="c9958-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c9958-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c9958-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c9958-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="c9958-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c9958-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9958-112">EXAMPLES</span></span>

### <span data-ttu-id="c9958-113">Exemplo 1: Remover um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="c9958-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="c9958-114">Este comando remove um esquema de conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="c9958-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="c9958-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c9958-115">PARAMETERS</span></span>

### <span data-ttu-id="c9958-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9958-116">-DefaultProfile</span></span>
<span data-ttu-id="c9958-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c9958-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9958-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c9958-118">-Force</span></span>
<span data-ttu-id="c9958-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c9958-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c9958-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c9958-120">-Name</span></span>
<span data-ttu-id="c9958-121">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c9958-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="c9958-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9958-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9958-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c9958-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c9958-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c9958-124">-SchemaName</span></span>
<span data-ttu-id="c9958-125">Especifica o nome de um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c9958-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="c9958-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9958-126">-Confirm</span></span>
<span data-ttu-id="c9958-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9958-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9958-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9958-128">-WhatIf</span></span>
<span data-ttu-id="c9958-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9958-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9958-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9958-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9958-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9958-131">CommonParameters</span></span>
<span data-ttu-id="c9958-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9958-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9958-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9958-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9958-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9958-134">INPUTS</span></span>

### <span data-ttu-id="c9958-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c9958-135">System.String</span></span>

## <span data-ttu-id="c9958-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c9958-136">OUTPUTS</span></span>

### <span data-ttu-id="c9958-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="c9958-137">System.Void</span></span>

## <span data-ttu-id="c9958-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="c9958-138">NOTES</span></span>

## <span data-ttu-id="c9958-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9958-139">RELATED LINKS</span></span>

[<span data-ttu-id="c9958-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="c9958-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="c9958-141">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="c9958-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="c9958-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="c9958-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


