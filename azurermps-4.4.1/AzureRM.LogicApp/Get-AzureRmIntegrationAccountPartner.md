---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: c74f4f89337d8fee4e6739cb145e9d2da0d4b81c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427891"
---
# <span data-ttu-id="3065d-101">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3065d-101">Get-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="3065d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3065d-102">SYNOPSIS</span></span>
<span data-ttu-id="3065d-103">Obtém os parceiros da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3065d-103">Gets integration account partners.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3065d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3065d-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3065d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3065d-105">DESCRIPTION</span></span>
<span data-ttu-id="3065d-106">O cmdlet **Get-AzureRmIntegrationAccountPartner** Obtém parceiros de conta de integração a partir de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3065d-106">The **Get-AzureRmIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="3065d-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do parceiro.</span><span class="sxs-lookup"><span data-stu-id="3065d-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="3065d-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="3065d-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3065d-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="3065d-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3065d-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3065d-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3065d-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="3065d-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3065d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3065d-112">EXAMPLES</span></span>

### <span data-ttu-id="3065d-113">Exemplo 1: obter um parceiro de conta de integração</span><span class="sxs-lookup"><span data-stu-id="3065d-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="3065d-114">Esse comando obtém o parceiro da conta de integração chamado IntegrationAccountPartner22.</span><span class="sxs-lookup"><span data-stu-id="3065d-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="3065d-115">Exemplo 2: obter um parceiro de conta de integração usando um nome de conta de integração</span><span class="sxs-lookup"><span data-stu-id="3065d-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="3065d-116">Esse comando obtém os parceiros da conta de integração da conta de integração chamada IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="3065d-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="3065d-117">OS</span><span class="sxs-lookup"><span data-stu-id="3065d-117">PARAMETERS</span></span>

### <span data-ttu-id="3065d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="3065d-118">-Name</span></span>
<span data-ttu-id="3065d-119">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3065d-119">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3065d-120">-Partnername</span><span class="sxs-lookup"><span data-stu-id="3065d-120">-PartnerName</span></span>
<span data-ttu-id="3065d-121">Especifica o nome do parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3065d-121">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="3065d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3065d-122">-ResourceGroupName</span></span>
<span data-ttu-id="3065d-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3065d-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3065d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3065d-124">-DefaultProfile</span></span>
<span data-ttu-id="3065d-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3065d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3065d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3065d-126">CommonParameters</span></span>
<span data-ttu-id="3065d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3065d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3065d-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3065d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3065d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3065d-129">INPUTS</span></span>

## <span data-ttu-id="3065d-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3065d-130">OUTPUTS</span></span>

### <span data-ttu-id="3065d-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3065d-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="3065d-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3065d-132">NOTES</span></span>

## <span data-ttu-id="3065d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3065d-133">RELATED LINKS</span></span>

[<span data-ttu-id="3065d-134">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3065d-134">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="3065d-135">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3065d-135">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="3065d-136">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3065d-136">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)

