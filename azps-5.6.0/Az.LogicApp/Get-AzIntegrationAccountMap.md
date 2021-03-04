---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: ef13fd50877076fb11382623b5e7950098204997
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886461"
---
# <span data-ttu-id="ad954-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ad954-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="ad954-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad954-102">SYNOPSIS</span></span>
<span data-ttu-id="ad954-103">Obtém um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ad954-103">Gets an integration account map.</span></span>

## <span data-ttu-id="ad954-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ad954-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad954-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ad954-105">DESCRIPTION</span></span>
<span data-ttu-id="ad954-106">O cmdlet **Get-AzIntegrationAccountMap** obtém o mapa de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad954-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="ad954-107">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do mapa.</span><span class="sxs-lookup"><span data-stu-id="ad954-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="ad954-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="ad954-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ad954-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="ad954-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ad954-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ad954-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ad954-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="ad954-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ad954-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad954-112">EXAMPLES</span></span>

### <span data-ttu-id="ad954-113">Exemplo 1: Obter um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="ad954-113">Example 1: Get an integration account map</span></span>
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

<span data-ttu-id="ad954-114">Este comando obtém um mapa de conta de integração chamado IntegrationAccountMap47 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ad954-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="ad954-115">Exemplo 2: Obter mapas de conta de integração pelo nome da conta de integração</span><span class="sxs-lookup"><span data-stu-id="ad954-115">Example 2: Get integration account maps by integration account name</span></span>
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

<span data-ttu-id="ad954-116">Este comando obtém os mapas de conta de integração pelo nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ad954-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="ad954-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ad954-117">PARAMETERS</span></span>

### <span data-ttu-id="ad954-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad954-118">-DefaultProfile</span></span>
<span data-ttu-id="ad954-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ad954-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad954-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="ad954-120">-MapName</span></span>
<span data-ttu-id="ad954-121">Especifica o nome de um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ad954-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="ad954-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="ad954-122">-MapType</span></span>
<span data-ttu-id="ad954-123">O tipo de mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ad954-123">The integration account map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad954-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ad954-124">-Name</span></span>
<span data-ttu-id="ad954-125">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ad954-125">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="ad954-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad954-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad954-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ad954-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad954-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad954-128">CommonParameters</span></span>
<span data-ttu-id="ad954-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad954-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad954-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad954-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad954-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad954-131">INPUTS</span></span>

### <span data-ttu-id="ad954-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ad954-132">System.String</span></span>

## <span data-ttu-id="ad954-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ad954-133">OUTPUTS</span></span>

### <span data-ttu-id="ad954-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ad954-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="ad954-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="ad954-135">NOTES</span></span>

## <span data-ttu-id="ad954-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad954-136">RELATED LINKS</span></span>

[<span data-ttu-id="ad954-137">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ad954-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="ad954-138">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ad954-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="ad954-139">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="ad954-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


