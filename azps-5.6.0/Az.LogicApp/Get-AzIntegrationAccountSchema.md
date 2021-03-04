---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: 5961741be40e52a705395d34d5b731715dff27a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886457"
---
# <span data-ttu-id="581b2-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="581b2-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="581b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="581b2-102">SYNOPSIS</span></span>
<span data-ttu-id="581b2-103">Obtém esquemas de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="581b2-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="581b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="581b2-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="581b2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="581b2-105">DESCRIPTION</span></span>
<span data-ttu-id="581b2-106">O cmdlet **Get-AzIntegrationAccountSchema** obtém esquemas de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="581b2-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="581b2-107">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="581b2-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="581b2-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="581b2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="581b2-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="581b2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="581b2-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="581b2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="581b2-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="581b2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="581b2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="581b2-112">EXAMPLES</span></span>

### <span data-ttu-id="581b2-113">Exemplo 1: Obter um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="581b2-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="581b2-114">Este comando obtém o esquema de conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="581b2-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="581b2-115">Exemplo 2: obter esquemas de conta de integração para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="581b2-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="581b2-116">Este comando obtém os esquemas de conta de integração do grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="581b2-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="581b2-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="581b2-117">PARAMETERS</span></span>

### <span data-ttu-id="581b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581b2-118">-DefaultProfile</span></span>
<span data-ttu-id="581b2-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="581b2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="581b2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="581b2-120">-Name</span></span>
<span data-ttu-id="581b2-121">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="581b2-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="581b2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="581b2-122">-ResourceGroupName</span></span>
<span data-ttu-id="581b2-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="581b2-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="581b2-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="581b2-124">-SchemaName</span></span>
<span data-ttu-id="581b2-125">Especifica o nome de um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="581b2-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="581b2-126">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="581b2-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="581b2-127">.</span><span class="sxs-lookup"><span data-stu-id="581b2-127">.</span></span>

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

### <span data-ttu-id="581b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581b2-128">CommonParameters</span></span>
<span data-ttu-id="581b2-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="581b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581b2-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="581b2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581b2-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="581b2-131">INPUTS</span></span>

### <span data-ttu-id="581b2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="581b2-132">System.String</span></span>

## <span data-ttu-id="581b2-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="581b2-133">OUTPUTS</span></span>

### <span data-ttu-id="581b2-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="581b2-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="581b2-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="581b2-135">NOTES</span></span>

## <span data-ttu-id="581b2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="581b2-136">RELATED LINKS</span></span>

[<span data-ttu-id="581b2-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="581b2-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="581b2-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="581b2-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="581b2-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="581b2-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


