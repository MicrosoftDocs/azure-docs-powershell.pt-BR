---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 39e78dfc27c325b9327d8ca7c27d800d656e3536
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770535"
---
# <span data-ttu-id="ca6a9-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ca6a9-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="ca6a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca6a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6a9-103">Obtém um mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-103">Gets an integration account map.</span></span>

## <span data-ttu-id="ca6a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca6a9-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca6a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca6a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ca6a9-106">O cmdlet **Get-AzIntegrationAccountMap** tem o mapa da conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="ca6a9-107">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do mapa.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="ca6a9-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ca6a9-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ca6a9-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ca6a9-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ca6a9-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca6a9-112">EXAMPLES</span></span>

### <span data-ttu-id="ca6a9-113">Exemplo 1: obter um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="ca6a9-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
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

<span data-ttu-id="ca6a9-114">Esse comando obtém um mapa de conta de integração chamado IntegrationAccountMap47 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="ca6a9-115">Exemplo 2: obter mapas da conta de integração por nome da conta de integração</span><span class="sxs-lookup"><span data-stu-id="ca6a9-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="ca6a9-116">Esse comando obtém os mapas da conta de integração por nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="ca6a9-117">OS</span><span class="sxs-lookup"><span data-stu-id="ca6a9-117">PARAMETERS</span></span>

### <span data-ttu-id="ca6a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6a9-118">-DefaultProfile</span></span>
<span data-ttu-id="ca6a9-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ca6a9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca6a9-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="ca6a9-120">-MapName</span></span>
<span data-ttu-id="ca6a9-121">Especifica o nome de um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="ca6a9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca6a9-122">-Name</span></span>
<span data-ttu-id="ca6a9-123">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-123">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="ca6a9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca6a9-124">-ResourceGroupName</span></span>
<span data-ttu-id="ca6a9-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ca6a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6a9-126">CommonParameters</span></span>
<span data-ttu-id="ca6a9-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca6a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6a9-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca6a9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6a9-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca6a9-129">INPUTS</span></span>

### <span data-ttu-id="ca6a9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ca6a9-130">System.String</span></span>

## <span data-ttu-id="ca6a9-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca6a9-131">OUTPUTS</span></span>

### <span data-ttu-id="ca6a9-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ca6a9-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="ca6a9-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca6a9-133">NOTES</span></span>

## <span data-ttu-id="ca6a9-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca6a9-134">RELATED LINKS</span></span>

[<span data-ttu-id="ca6a9-135">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ca6a9-135">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="ca6a9-136">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ca6a9-136">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="ca6a9-137">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ca6a9-137">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


