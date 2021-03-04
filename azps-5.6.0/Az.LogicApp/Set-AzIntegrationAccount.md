---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 8a6808c19dda99f6d76280fc8519a6afc658d9ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888356"
---
# <span data-ttu-id="7b2a5-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7b2a5-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="7b2a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2a5-103">Modifica uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-103">Modifies an integration account.</span></span>

## <span data-ttu-id="7b2a5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7b2a5-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b2a5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7b2a5-105">DESCRIPTION</span></span>
<span data-ttu-id="7b2a5-106">O cmdlet **Set-AzIntegrationAccount** modifica uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="7b2a5-107">Este cmdlet retorna um objeto que representa a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="7b2a5-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7b2a5-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7b2a5-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7b2a5-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7b2a5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b2a5-112">EXAMPLES</span></span>

### <span data-ttu-id="7b2a5-113">Exemplo 1: Modificar uma conta de integração</span><span class="sxs-lookup"><span data-stu-id="7b2a5-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="7b2a5-114">Este comando modifica uma conta de integração chamada IntegrationAccount31 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="7b2a5-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7b2a5-115">PARAMETERS</span></span>

### <span data-ttu-id="7b2a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2a5-116">-DefaultProfile</span></span>
<span data-ttu-id="7b2a5-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7b2a5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b2a5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7b2a5-118">-Force</span></span>
<span data-ttu-id="7b2a5-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b2a5-120">-Location</span><span class="sxs-lookup"><span data-stu-id="7b2a5-120">-Location</span></span>
<span data-ttu-id="7b2a5-121">Especifica um local para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-121">Specifies a location for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2a5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7b2a5-122">-Name</span></span>
<span data-ttu-id="7b2a5-123">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2a5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b2a5-124">-ResourceGroupName</span></span>
<span data-ttu-id="7b2a5-125">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7b2a5-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="7b2a5-126">-Sku</span></span>
<span data-ttu-id="7b2a5-127">Especifica um nome SKU para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2a5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b2a5-128">-Confirm</span></span>
<span data-ttu-id="7b2a5-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b2a5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b2a5-130">-WhatIf</span></span>
<span data-ttu-id="7b2a5-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b2a5-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b2a5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2a5-133">CommonParameters</span></span>
<span data-ttu-id="7b2a5-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b2a5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2a5-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b2a5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2a5-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b2a5-136">INPUTS</span></span>

### <span data-ttu-id="7b2a5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7b2a5-137">System.String</span></span>

## <span data-ttu-id="7b2a5-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7b2a5-138">OUTPUTS</span></span>

### <span data-ttu-id="7b2a5-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7b2a5-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="7b2a5-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="7b2a5-140">NOTES</span></span>

## <span data-ttu-id="7b2a5-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b2a5-141">RELATED LINKS</span></span>

[<span data-ttu-id="7b2a5-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7b2a5-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="7b2a5-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7b2a5-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="7b2a5-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7b2a5-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


