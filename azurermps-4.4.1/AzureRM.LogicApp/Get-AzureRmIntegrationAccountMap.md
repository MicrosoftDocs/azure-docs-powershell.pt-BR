---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 6f1f58f5f25b3e3ef4782bcc0ea8a4b3170eed81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427894"
---
# <span data-ttu-id="f78a5-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f78a5-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="f78a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f78a5-102">SYNOPSIS</span></span>
<span data-ttu-id="f78a5-103">Obtém um mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f78a5-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f78a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f78a5-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f78a5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f78a5-105">DESCRIPTION</span></span>
<span data-ttu-id="f78a5-106">O cmdlet **Get-AzureRmIntegrationAccountMap** tem o mapa da conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f78a5-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="f78a5-107">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do mapa.</span><span class="sxs-lookup"><span data-stu-id="f78a5-107">Specifying the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="f78a5-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="f78a5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f78a5-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="f78a5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f78a5-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f78a5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f78a5-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="f78a5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f78a5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f78a5-112">EXAMPLES</span></span>

### <span data-ttu-id="f78a5-113">Exemplo 1: obter um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="f78a5-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="f78a5-114">Esse comando obtém um mapa de conta de integração chamado IntegrationAccountMap47 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="f78a5-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="f78a5-115">Exemplo 2: obter mapas da conta de integração por nome da conta de integração</span><span class="sxs-lookup"><span data-stu-id="f78a5-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="f78a5-116">Esse comando obtém os mapas da conta de integração por nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f78a5-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="f78a5-117">OS</span><span class="sxs-lookup"><span data-stu-id="f78a5-117">PARAMETERS</span></span>

### <span data-ttu-id="f78a5-118">-MapName</span><span class="sxs-lookup"><span data-stu-id="f78a5-118">-MapName</span></span>
<span data-ttu-id="f78a5-119">Especifica o nome de um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f78a5-119">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="f78a5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f78a5-120">-Name</span></span>
<span data-ttu-id="f78a5-121">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="f78a5-121">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="f78a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f78a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="f78a5-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f78a5-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f78a5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f78a5-124">-DefaultProfile</span></span>
<span data-ttu-id="f78a5-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f78a5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f78a5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f78a5-126">CommonParameters</span></span>
<span data-ttu-id="f78a5-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f78a5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f78a5-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f78a5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f78a5-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f78a5-129">INPUTS</span></span>

## <span data-ttu-id="f78a5-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f78a5-130">OUTPUTS</span></span>

### <span data-ttu-id="f78a5-131">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f78a5-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="f78a5-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f78a5-132">NOTES</span></span>

## <span data-ttu-id="f78a5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f78a5-133">RELATED LINKS</span></span>

[<span data-ttu-id="f78a5-134">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f78a5-134">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="f78a5-135">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f78a5-135">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="f78a5-136">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="f78a5-136">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


