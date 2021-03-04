---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: c519a747a36db3ed2a2365052ac00a1166c45aed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887986"
---
# <span data-ttu-id="75f9a-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="75f9a-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="75f9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="75f9a-103">Obtém contas de integração.</span><span class="sxs-lookup"><span data-stu-id="75f9a-103">Gets integration accounts.</span></span>

## <span data-ttu-id="75f9a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="75f9a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75f9a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="75f9a-105">DESCRIPTION</span></span>
<span data-ttu-id="75f9a-106">O cmdlet **Get-AzIntegrationAccount** obtém contas de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75f9a-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="75f9a-107">Especifique um nome de conta de integração e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75f9a-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="75f9a-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="75f9a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="75f9a-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="75f9a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="75f9a-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="75f9a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="75f9a-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="75f9a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="75f9a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="75f9a-112">EXAMPLES</span></span>

### <span data-ttu-id="75f9a-113">Exemplo 1: Obter uma conta de integração pelo nome</span><span class="sxs-lookup"><span data-stu-id="75f9a-113">Example 1: Get an integration account by name</span></span>
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

<span data-ttu-id="75f9a-114">Este comando obtém uma conta de integração chamada IntegrationAccount31 do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="75f9a-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="75f9a-115">Exemplo 2: obter contas de integração em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="75f9a-115">Example 2: Get integration accounts in a resource group</span></span>
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

<span data-ttu-id="75f9a-116">Este comando obtém contas de integração de um grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="75f9a-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="75f9a-117">Exemplo 3: Obter todas as contas de integração</span><span class="sxs-lookup"><span data-stu-id="75f9a-117">Example 3: Get all integration accounts</span></span>
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

<span data-ttu-id="75f9a-118">Este comando obtém todas as contas de integração em sua assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="75f9a-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="75f9a-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="75f9a-119">PARAMETERS</span></span>

### <span data-ttu-id="75f9a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f9a-120">-DefaultProfile</span></span>
<span data-ttu-id="75f9a-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="75f9a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75f9a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="75f9a-122">-Name</span></span>
<span data-ttu-id="75f9a-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="75f9a-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="75f9a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f9a-124">-ResourceGroupName</span></span>
<span data-ttu-id="75f9a-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="75f9a-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="75f9a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f9a-126">CommonParameters</span></span>
<span data-ttu-id="75f9a-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f9a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f9a-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75f9a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f9a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75f9a-129">INPUTS</span></span>

### <span data-ttu-id="75f9a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="75f9a-130">System.String</span></span>

## <span data-ttu-id="75f9a-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="75f9a-131">OUTPUTS</span></span>

### <span data-ttu-id="75f9a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="75f9a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="75f9a-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="75f9a-133">NOTES</span></span>

## <span data-ttu-id="75f9a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="75f9a-134">RELATED LINKS</span></span>

[<span data-ttu-id="75f9a-135">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="75f9a-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="75f9a-136">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="75f9a-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="75f9a-137">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="75f9a-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="75f9a-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="75f9a-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


