---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: c34146079b419bceabfec1a2b9deb67c8eec658f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427886"
---
# <span data-ttu-id="dca01-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dca01-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="dca01-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dca01-102">SYNOPSIS</span></span>
<span data-ttu-id="dca01-103">Obtém esquemas da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="dca01-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dca01-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dca01-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dca01-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dca01-105">DESCRIPTION</span></span>
<span data-ttu-id="dca01-106">O cmdlet **Get-AzureRmIntegrationAccountSchema** tem esquemas de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="dca01-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="dca01-107">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="dca01-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="dca01-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="dca01-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dca01-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="dca01-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dca01-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="dca01-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dca01-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="dca01-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dca01-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dca01-112">EXAMPLES</span></span>

### <span data-ttu-id="dca01-113">Exemplo 1: obter um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="dca01-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
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

<span data-ttu-id="dca01-114">Esse comando obtém o esquema da conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="dca01-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="dca01-115">Exemplo 2: obter esquemas da conta de integração para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="dca01-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="dca01-116">Esse comando obtém os esquemas da conta de integração do grupo de recursos chamado ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="dca01-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="dca01-117">OS</span><span class="sxs-lookup"><span data-stu-id="dca01-117">PARAMETERS</span></span>

### <span data-ttu-id="dca01-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dca01-118">-Name</span></span>
<span data-ttu-id="dca01-119">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="dca01-119">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="dca01-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dca01-120">-ResourceGroupName</span></span>
<span data-ttu-id="dca01-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dca01-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dca01-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="dca01-122">-SchemaName</span></span>
<span data-ttu-id="dca01-123">Especifica o nome de um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="dca01-123">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="dca01-124">Especifica o nome de um esquema.</span><span class="sxs-lookup"><span data-stu-id="dca01-124">Specifies the name of a schema.</span></span>
<span data-ttu-id="dca01-125">.</span><span class="sxs-lookup"><span data-stu-id="dca01-125">.</span></span>

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

### <span data-ttu-id="dca01-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dca01-126">-DefaultProfile</span></span>
<span data-ttu-id="dca01-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dca01-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dca01-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dca01-128">CommonParameters</span></span>
<span data-ttu-id="dca01-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dca01-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dca01-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dca01-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dca01-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dca01-131">INPUTS</span></span>

## <span data-ttu-id="dca01-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dca01-132">OUTPUTS</span></span>

### <span data-ttu-id="dca01-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dca01-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="dca01-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dca01-134">NOTES</span></span>

## <span data-ttu-id="dca01-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dca01-135">RELATED LINKS</span></span>

[<span data-ttu-id="dca01-136">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dca01-136">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="dca01-137">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dca01-137">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="dca01-138">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="dca01-138">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)

