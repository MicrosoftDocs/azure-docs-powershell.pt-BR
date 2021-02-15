---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 3bb20e0314e95f2586c0bd8585c7937c4d6ca5b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114788"
---
# <span data-ttu-id="35433-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="35433-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="35433-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35433-102">SYNOPSIS</span></span>
<span data-ttu-id="35433-103">Modifica uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35433-103">Modifies an integration account.</span></span>

## <span data-ttu-id="35433-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35433-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35433-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="35433-105">DESCRIPTION</span></span>
<span data-ttu-id="35433-106">O **cmdlet Set-AzIntegrationAccount** modifica uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35433-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="35433-107">Esse cmdlet retorna um objeto que representa a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35433-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="35433-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="35433-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="35433-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="35433-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="35433-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="35433-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="35433-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="35433-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="35433-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="35433-112">EXAMPLES</span></span>

### <span data-ttu-id="35433-113">Exemplo 1: Modificar uma conta de integração</span><span class="sxs-lookup"><span data-stu-id="35433-113">Example 1: Modify an integration account</span></span>
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

<span data-ttu-id="35433-114">Esse comando modifica uma conta de integração chamada IntegrationAccount31 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="35433-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="35433-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35433-115">PARAMETERS</span></span>

### <span data-ttu-id="35433-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35433-116">-DefaultProfile</span></span>
<span data-ttu-id="35433-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="35433-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35433-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="35433-118">-Force</span></span>
<span data-ttu-id="35433-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="35433-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35433-120">-Local</span><span class="sxs-lookup"><span data-stu-id="35433-120">-Location</span></span>
<span data-ttu-id="35433-121">Especifica um local para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35433-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="35433-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="35433-122">-Name</span></span>
<span data-ttu-id="35433-123">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35433-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="35433-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35433-124">-ResourceGroupName</span></span>
<span data-ttu-id="35433-125">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35433-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="35433-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="35433-126">-Sku</span></span>
<span data-ttu-id="35433-127">Especifica um nome SKU para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="35433-127">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="35433-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="35433-128">-Confirm</span></span>
<span data-ttu-id="35433-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35433-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35433-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35433-130">-WhatIf</span></span>
<span data-ttu-id="35433-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="35433-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35433-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35433-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35433-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35433-133">CommonParameters</span></span>
<span data-ttu-id="35433-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35433-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35433-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35433-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35433-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="35433-136">INPUTS</span></span>

### <span data-ttu-id="35433-137">System.String</span><span class="sxs-lookup"><span data-stu-id="35433-137">System.String</span></span>

## <span data-ttu-id="35433-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="35433-138">OUTPUTS</span></span>

### <span data-ttu-id="35433-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="35433-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="35433-140">Notas</span><span class="sxs-lookup"><span data-stu-id="35433-140">NOTES</span></span>

## <span data-ttu-id="35433-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35433-141">RELATED LINKS</span></span>

[<span data-ttu-id="35433-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="35433-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="35433-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="35433-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="35433-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="35433-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


