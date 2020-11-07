---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944339"
---
# <span data-ttu-id="cd425-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cd425-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="cd425-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd425-102">SYNOPSIS</span></span>
<span data-ttu-id="cd425-103">Cria uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cd425-103">Creates an integration account.</span></span>

## <span data-ttu-id="cd425-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd425-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd425-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd425-105">DESCRIPTION</span></span>
<span data-ttu-id="cd425-106">O cmdlet **New-AzIntegrationAccount** cria uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cd425-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="cd425-107">Esse cmdlet retorna um objeto que representa a conta de integração. Especifique um nome, local, nome do grupo de recursos e nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="cd425-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="cd425-108">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="cd425-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="cd425-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="cd425-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cd425-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="cd425-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cd425-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cd425-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cd425-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="cd425-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cd425-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd425-113">EXAMPLES</span></span>

### <span data-ttu-id="cd425-114">Exemplo 1: criar uma conta de integração</span><span class="sxs-lookup"><span data-stu-id="cd425-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="cd425-115">Esse comando cria uma conta de integração chamada IntegrationAccount31 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="cd425-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="cd425-116">OS</span><span class="sxs-lookup"><span data-stu-id="cd425-116">PARAMETERS</span></span>

### <span data-ttu-id="cd425-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd425-117">-DefaultProfile</span></span>
<span data-ttu-id="cd425-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cd425-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd425-119">-Local</span><span class="sxs-lookup"><span data-stu-id="cd425-119">-Location</span></span>
<span data-ttu-id="cd425-120">Especifica um local para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cd425-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="cd425-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd425-121">-Name</span></span>
<span data-ttu-id="cd425-122">Especifica um nome para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cd425-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="cd425-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd425-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd425-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd425-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cd425-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="cd425-125">-Sku</span></span>
<span data-ttu-id="cd425-126">Especifica um nome de SKU para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="cd425-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd425-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd425-127">-Confirm</span></span>
<span data-ttu-id="cd425-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd425-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd425-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd425-129">-WhatIf</span></span>
<span data-ttu-id="cd425-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd425-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd425-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd425-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd425-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd425-132">CommonParameters</span></span>
<span data-ttu-id="cd425-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd425-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd425-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd425-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd425-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd425-135">INPUTS</span></span>

### <span data-ttu-id="cd425-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cd425-136">System.String</span></span>

## <span data-ttu-id="cd425-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd425-137">OUTPUTS</span></span>

### <span data-ttu-id="cd425-138">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cd425-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="cd425-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd425-139">NOTES</span></span>

## <span data-ttu-id="cd425-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd425-140">RELATED LINKS</span></span>

[<span data-ttu-id="cd425-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cd425-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="cd425-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cd425-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="cd425-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cd425-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


