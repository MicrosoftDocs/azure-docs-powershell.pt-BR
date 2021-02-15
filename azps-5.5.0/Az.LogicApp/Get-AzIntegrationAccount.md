---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114797"
---
# <span data-ttu-id="4c8eb-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4c8eb-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="4c8eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c8eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4c8eb-103">Obtém contas de integração.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-103">Gets integration accounts.</span></span>

## <span data-ttu-id="4c8eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c8eb-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c8eb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c8eb-105">DESCRIPTION</span></span>
<span data-ttu-id="4c8eb-106">O **cmdlet Get-AzIntegrationAccount obtém** contas de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="4c8eb-107">Especifique o nome de uma conta de integração e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="4c8eb-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4c8eb-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4c8eb-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4c8eb-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4c8eb-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c8eb-112">EXAMPLES</span></span>

### <span data-ttu-id="4c8eb-113">Exemplo 1: Obter uma conta de integração por nome</span><span class="sxs-lookup"><span data-stu-id="4c8eb-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="4c8eb-114">Esse comando obtém uma conta de integração chamada IntegrationAccount31 do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="4c8eb-115">Exemplo 2: Obter contas de integração em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4c8eb-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="4c8eb-116">Esse comando obtém contas de integração de um grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="4c8eb-117">Exemplo 3: Obter todas as contas de integração</span><span class="sxs-lookup"><span data-stu-id="4c8eb-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="4c8eb-118">Esse comando obtém todas as contas de integração em sua assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="4c8eb-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c8eb-119">PARAMETERS</span></span>

### <span data-ttu-id="4c8eb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c8eb-120">-DefaultProfile</span></span>
<span data-ttu-id="4c8eb-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4c8eb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c8eb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c8eb-122">-Name</span></span>
<span data-ttu-id="4c8eb-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c8eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c8eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c8eb-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4c8eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c8eb-126">CommonParameters</span></span>
<span data-ttu-id="4c8eb-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c8eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c8eb-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c8eb-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c8eb-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="4c8eb-129">INPUTS</span></span>

### <span data-ttu-id="4c8eb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4c8eb-130">System.String</span></span>

## <span data-ttu-id="4c8eb-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="4c8eb-131">OUTPUTS</span></span>

### <span data-ttu-id="4c8eb-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4c8eb-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="4c8eb-133">Notas</span><span class="sxs-lookup"><span data-stu-id="4c8eb-133">NOTES</span></span>

## <span data-ttu-id="4c8eb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c8eb-134">RELATED LINKS</span></span>

[<span data-ttu-id="4c8eb-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="4c8eb-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="4c8eb-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4c8eb-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="4c8eb-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4c8eb-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="4c8eb-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4c8eb-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


