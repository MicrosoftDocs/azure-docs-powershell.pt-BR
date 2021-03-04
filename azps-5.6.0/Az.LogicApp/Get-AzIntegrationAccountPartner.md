---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: 1819f8978ef29235743f9b4095d770f3b34c4b9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886459"
---
# <span data-ttu-id="f12fe-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f12fe-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="f12fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f12fe-102">SYNOPSIS</span></span>
<span data-ttu-id="f12fe-103">Obtém parceiros de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f12fe-103">Gets integration account partners.</span></span>

## <span data-ttu-id="f12fe-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f12fe-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f12fe-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f12fe-105">DESCRIPTION</span></span>
<span data-ttu-id="f12fe-106">O cmdlet **Get-AzIntegrationAccountPartner obtém** parceiros de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f12fe-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="f12fe-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do parceiro.</span><span class="sxs-lookup"><span data-stu-id="f12fe-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="f12fe-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="f12fe-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f12fe-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="f12fe-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f12fe-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f12fe-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f12fe-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="f12fe-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f12fe-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f12fe-112">EXAMPLES</span></span>

### <span data-ttu-id="f12fe-113">Exemplo 1: obter um parceiro de conta de integração</span><span class="sxs-lookup"><span data-stu-id="f12fe-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="f12fe-114">Este comando obtém o parceiro de conta de integração chamado IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="f12fe-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="f12fe-115">Exemplo 2: obter parceiros de conta de integração usando um nome de conta de integração</span><span class="sxs-lookup"><span data-stu-id="f12fe-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="f12fe-116">Este comando obtém os parceiros de conta de integração da conta de integração chamada IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="f12fe-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="f12fe-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f12fe-117">PARAMETERS</span></span>

### <span data-ttu-id="f12fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f12fe-118">-DefaultProfile</span></span>
<span data-ttu-id="f12fe-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f12fe-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f12fe-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f12fe-120">-Name</span></span>
<span data-ttu-id="f12fe-121">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f12fe-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="f12fe-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="f12fe-122">-PartnerName</span></span>
<span data-ttu-id="f12fe-123">Especifica o nome do parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f12fe-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f12fe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f12fe-124">-ResourceGroupName</span></span>
<span data-ttu-id="f12fe-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f12fe-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f12fe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f12fe-126">CommonParameters</span></span>
<span data-ttu-id="f12fe-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f12fe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f12fe-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f12fe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f12fe-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f12fe-129">INPUTS</span></span>

### <span data-ttu-id="f12fe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f12fe-130">System.String</span></span>

## <span data-ttu-id="f12fe-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f12fe-131">OUTPUTS</span></span>

### <span data-ttu-id="f12fe-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f12fe-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="f12fe-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="f12fe-133">NOTES</span></span>

## <span data-ttu-id="f12fe-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f12fe-134">RELATED LINKS</span></span>

[<span data-ttu-id="f12fe-135">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f12fe-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f12fe-136">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f12fe-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f12fe-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f12fe-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


