---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: 441681cd33fe7715fbbb6fb244848c287f14ebb6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427903"
---
# <span data-ttu-id="15fa9-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15fa9-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="15fa9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="15fa9-103">Obtém contas de integração.</span><span class="sxs-lookup"><span data-stu-id="15fa9-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15fa9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15fa9-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15fa9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="15fa9-106">O cmdlet **Get-AzureRmIntegrationAccount** Obtém contas de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15fa9-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="15fa9-107">Especifique o nome da conta de integração e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15fa9-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="15fa9-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="15fa9-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="15fa9-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="15fa9-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="15fa9-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="15fa9-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="15fa9-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="15fa9-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="15fa9-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15fa9-112">EXAMPLES</span></span>

### <span data-ttu-id="15fa9-113">Exemplo 1: obter uma conta de integração por nome</span><span class="sxs-lookup"><span data-stu-id="15fa9-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="15fa9-114">Esse comando obtém uma conta de integração chamada IntegrationAccount31 do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="15fa9-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="15fa9-115">Exemplo 2: obter contas de integração em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="15fa9-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="15fa9-116">Esse comando obtém contas de integração de um grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="15fa9-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="15fa9-117">Exemplo 3: obter todas as contas de integração</span><span class="sxs-lookup"><span data-stu-id="15fa9-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzureRmIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="15fa9-118">Esse comando obtém todas as contas de integração na sua assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="15fa9-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="15fa9-119">OS</span><span class="sxs-lookup"><span data-stu-id="15fa9-119">PARAMETERS</span></span>

### <span data-ttu-id="15fa9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="15fa9-120">-Name</span></span>
<span data-ttu-id="15fa9-121">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="15fa9-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="15fa9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15fa9-122">-ResourceGroupName</span></span>
<span data-ttu-id="15fa9-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15fa9-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="15fa9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fa9-124">-DefaultProfile</span></span>
<span data-ttu-id="15fa9-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15fa9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15fa9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fa9-126">CommonParameters</span></span>
<span data-ttu-id="15fa9-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15fa9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fa9-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15fa9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fa9-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15fa9-129">INPUTS</span></span>

## <span data-ttu-id="15fa9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15fa9-130">OUTPUTS</span></span>

### <span data-ttu-id="15fa9-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15fa9-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="15fa9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15fa9-132">NOTES</span></span>

## <span data-ttu-id="15fa9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15fa9-133">RELATED LINKS</span></span>

[<span data-ttu-id="15fa9-134">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="15fa9-134">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="15fa9-135">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15fa9-135">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="15fa9-136">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15fa9-136">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="15fa9-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="15fa9-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


