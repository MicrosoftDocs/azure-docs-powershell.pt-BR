---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccount.md
ms.openlocfilehash: ee96c446ee0517363535b09ee320e04db7aeba38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432485"
---
# <span data-ttu-id="ed17d-101">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed17d-101">Get-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="ed17d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed17d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed17d-103">Obtém contas de integração.</span><span class="sxs-lookup"><span data-stu-id="ed17d-103">Gets integration accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed17d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed17d-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed17d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed17d-105">DESCRIPTION</span></span>
<span data-ttu-id="ed17d-106">O cmdlet **Get-AzureRmIntegrationAccount** Obtém contas de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed17d-106">The **Get-AzureRmIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="ed17d-107">Especifique o nome da conta de integração e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed17d-107">Specify an integration account name and resource group name.</span></span>

<span data-ttu-id="ed17d-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="ed17d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ed17d-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="ed17d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ed17d-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ed17d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ed17d-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="ed17d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ed17d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed17d-112">EXAMPLES</span></span>

### <span data-ttu-id="ed17d-113">Exemplo 1: obter uma conta de integração por nome</span><span class="sxs-lookup"><span data-stu-id="ed17d-113">Example 1: Get an integration account by name</span></span>
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

<span data-ttu-id="ed17d-114">Esse comando obtém uma conta de integração chamada IntegrationAccount31 do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ed17d-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="ed17d-115">Exemplo 2: obter contas de integração em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ed17d-115">Example 2: Get integration accounts in a resource group</span></span>
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

<span data-ttu-id="ed17d-116">Esse comando obtém contas de integração de um grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ed17d-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ed17d-117">Exemplo 3: obter todas as contas de integração</span><span class="sxs-lookup"><span data-stu-id="ed17d-117">Example 3: Get all integration accounts</span></span>
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

<span data-ttu-id="ed17d-118">Esse comando obtém todas as contas de integração na sua assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ed17d-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="ed17d-119">OS</span><span class="sxs-lookup"><span data-stu-id="ed17d-119">PARAMETERS</span></span>

### <span data-ttu-id="ed17d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed17d-120">-DefaultProfile</span></span>
<span data-ttu-id="ed17d-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ed17d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed17d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed17d-122">-Name</span></span>
<span data-ttu-id="ed17d-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ed17d-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed17d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed17d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ed17d-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed17d-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed17d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed17d-126">CommonParameters</span></span>
<span data-ttu-id="ed17d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed17d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed17d-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed17d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed17d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed17d-129">INPUTS</span></span>

### <span data-ttu-id="ed17d-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ed17d-130">None</span></span>
<span data-ttu-id="ed17d-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ed17d-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ed17d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed17d-132">OUTPUTS</span></span>

### <span data-ttu-id="ed17d-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed17d-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="ed17d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed17d-134">NOTES</span></span>

## <span data-ttu-id="ed17d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed17d-135">RELATED LINKS</span></span>

[<span data-ttu-id="ed17d-136">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="ed17d-136">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="ed17d-137">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed17d-137">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="ed17d-138">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed17d-138">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="ed17d-139">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="ed17d-139">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


