---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: 7183078623c3be1826c98712fa41524643a4a68c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430909"
---
# <span data-ttu-id="3cb51-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3cb51-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="3cb51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3cb51-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb51-103">Cria uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3cb51-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cb51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3cb51-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cb51-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3cb51-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb51-106">O cmdlet **New-AzureRmIntegrationAccount** cria uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3cb51-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="3cb51-107">Esse cmdlet retorna um objeto que representa a conta de integração. Especifique um nome, local, nome do grupo de recursos e nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="3cb51-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="3cb51-108">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="3cb51-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="3cb51-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="3cb51-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3cb51-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="3cb51-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3cb51-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3cb51-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3cb51-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="3cb51-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3cb51-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3cb51-113">EXAMPLES</span></span>

### <span data-ttu-id="3cb51-114">Exemplo 1: criar uma conta de integração</span><span class="sxs-lookup"><span data-stu-id="3cb51-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="3cb51-115">Esse comando cria uma conta de integração chamada IntegrationAccount31 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="3cb51-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="3cb51-116">OS</span><span class="sxs-lookup"><span data-stu-id="3cb51-116">PARAMETERS</span></span>

### <span data-ttu-id="3cb51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb51-117">-DefaultProfile</span></span>
<span data-ttu-id="3cb51-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3cb51-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cb51-119">-Local</span><span class="sxs-lookup"><span data-stu-id="3cb51-119">-Location</span></span>
<span data-ttu-id="3cb51-120">Especifica um local para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3cb51-120">Specifies a location for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb51-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3cb51-121">-Name</span></span>
<span data-ttu-id="3cb51-122">Especifica um nome para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3cb51-122">Specifies a name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb51-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb51-123">-ResourceGroupName</span></span>
<span data-ttu-id="3cb51-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3cb51-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb51-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="3cb51-125">-Sku</span></span>
<span data-ttu-id="3cb51-126">Especifica um nome de SKU para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3cb51-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="3cb51-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3cb51-127">-Confirm</span></span>
<span data-ttu-id="3cb51-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cb51-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb51-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb51-129">-WhatIf</span></span>
<span data-ttu-id="3cb51-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3cb51-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb51-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3cb51-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb51-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb51-132">CommonParameters</span></span>
<span data-ttu-id="3cb51-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb51-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb51-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cb51-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb51-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3cb51-135">INPUTS</span></span>

### <span data-ttu-id="3cb51-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3cb51-136">System.String</span></span>

## <span data-ttu-id="3cb51-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3cb51-137">OUTPUTS</span></span>

### <span data-ttu-id="3cb51-138">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3cb51-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="3cb51-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3cb51-139">NOTES</span></span>

## <span data-ttu-id="3cb51-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3cb51-140">RELATED LINKS</span></span>

[<span data-ttu-id="3cb51-141">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3cb51-141">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="3cb51-142">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3cb51-142">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="3cb51-143">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3cb51-143">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

