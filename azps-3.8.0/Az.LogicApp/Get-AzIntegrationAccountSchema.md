---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777709"
---
# <span data-ttu-id="604e7-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="604e7-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="604e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="604e7-102">SYNOPSIS</span></span>
<span data-ttu-id="604e7-103">Obtém esquemas da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="604e7-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="604e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="604e7-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="604e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="604e7-105">DESCRIPTION</span></span>
<span data-ttu-id="604e7-106">O cmdlet **Get-AzIntegrationAccountSchema** tem esquemas de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="604e7-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="604e7-107">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="604e7-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="604e7-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="604e7-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="604e7-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="604e7-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="604e7-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="604e7-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="604e7-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="604e7-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="604e7-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="604e7-112">EXAMPLES</span></span>

### <span data-ttu-id="604e7-113">Exemplo 1: obter um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="604e7-113">Example 1: Get an integration account schema</span></span>
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

<span data-ttu-id="604e7-114">Esse comando obtém o esquema da conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="604e7-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="604e7-115">Exemplo 2: obter esquemas da conta de integração para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="604e7-115">Example 2: Get integration account schemas for a resource group</span></span>
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

<span data-ttu-id="604e7-116">Esse comando obtém os esquemas da conta de integração do grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="604e7-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="604e7-117">OS</span><span class="sxs-lookup"><span data-stu-id="604e7-117">PARAMETERS</span></span>

### <span data-ttu-id="604e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="604e7-118">-DefaultProfile</span></span>
<span data-ttu-id="604e7-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="604e7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="604e7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="604e7-120">-Name</span></span>
<span data-ttu-id="604e7-121">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="604e7-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="604e7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="604e7-122">-ResourceGroupName</span></span>
<span data-ttu-id="604e7-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="604e7-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="604e7-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="604e7-124">-SchemaName</span></span>
<span data-ttu-id="604e7-125">Especifica o nome de um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="604e7-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="604e7-126">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="604e7-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="604e7-127">.</span><span class="sxs-lookup"><span data-stu-id="604e7-127">.</span></span>

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

### <span data-ttu-id="604e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604e7-128">CommonParameters</span></span>
<span data-ttu-id="604e7-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="604e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604e7-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="604e7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604e7-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="604e7-131">INPUTS</span></span>

### <span data-ttu-id="604e7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="604e7-132">System.String</span></span>

## <span data-ttu-id="604e7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="604e7-133">OUTPUTS</span></span>

### <span data-ttu-id="604e7-134">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="604e7-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="604e7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="604e7-135">NOTES</span></span>

## <span data-ttu-id="604e7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="604e7-136">RELATED LINKS</span></span>

[<span data-ttu-id="604e7-137">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="604e7-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="604e7-138">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="604e7-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="604e7-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="604e7-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


