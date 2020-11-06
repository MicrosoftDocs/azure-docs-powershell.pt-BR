---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: e483d2f88f12655283c94d8c42e9926e4dd6cddb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596050"
---
# <span data-ttu-id="40004-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="40004-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="40004-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40004-102">SYNOPSIS</span></span>
<span data-ttu-id="40004-103">Cria um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="40004-103">Creates an integration account map.</span></span>

## <span data-ttu-id="40004-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40004-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40004-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40004-105">DESCRIPTION</span></span>
<span data-ttu-id="40004-106">O cmdlet **New-AzIntegrationAccountMap** cria um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="40004-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="40004-107">Esse cmdlet retorna um objeto que representa o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="40004-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="40004-108">Especificando o nome da conta de integração, o nome do grupo de recursos, o nome do mapa e a definição do mapa.</span><span class="sxs-lookup"><span data-stu-id="40004-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="40004-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="40004-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="40004-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="40004-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="40004-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="40004-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="40004-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="40004-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="40004-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="40004-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="40004-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40004-114">EXAMPLES</span></span>

### <span data-ttu-id="40004-115">Exemplo 1: criar um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="40004-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="40004-116">Esse comando cria o mapa da conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="40004-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="40004-117">O comando especifica uma definição de mapa armazenada na variável $MapContent por um comando anterior.</span><span class="sxs-lookup"><span data-stu-id="40004-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="40004-118">OS</span><span class="sxs-lookup"><span data-stu-id="40004-118">PARAMETERS</span></span>

### <span data-ttu-id="40004-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="40004-119">-ContentType</span></span>
<span data-ttu-id="40004-120">Especifica um tipo de conteúdo para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="40004-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="40004-121">Esse cmdlet dá suporte a Application/XML como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="40004-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="40004-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40004-122">-DefaultProfile</span></span>
<span data-ttu-id="40004-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="40004-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40004-124">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="40004-124">-MapDefinition</span></span>
<span data-ttu-id="40004-125">Especifica um objeto de definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="40004-125">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="40004-126">Especifique esse parâmetro ou o parâmetro *MapFilePath* .</span><span class="sxs-lookup"><span data-stu-id="40004-126">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="40004-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="40004-127">-MapFilePath</span></span>
<span data-ttu-id="40004-128">Especifica o caminho do arquivo de uma definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="40004-128">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="40004-129">Especifique esse parâmetro ou o parâmetro *MapDefinition* .</span><span class="sxs-lookup"><span data-stu-id="40004-129">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="40004-130">-MapName</span><span class="sxs-lookup"><span data-stu-id="40004-130">-MapName</span></span>
<span data-ttu-id="40004-131">Especifica um nome para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="40004-131">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="40004-132">-MapType</span><span class="sxs-lookup"><span data-stu-id="40004-132">-MapType</span></span>
<span data-ttu-id="40004-133">Especifica o tipo do mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="40004-133">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="40004-134">Esse cmdlet dá suporte a XSLT como um tipo de mapa.</span><span class="sxs-lookup"><span data-stu-id="40004-134">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="40004-135">-Metadados</span><span class="sxs-lookup"><span data-stu-id="40004-135">-Metadata</span></span>
<span data-ttu-id="40004-136">Especifica um objeto de metadados para o mapa.</span><span class="sxs-lookup"><span data-stu-id="40004-136">Specifies a metadata object for the map.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40004-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="40004-137">-Name</span></span>
<span data-ttu-id="40004-138">Especifica um nome para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="40004-138">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="40004-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40004-139">-ResourceGroupName</span></span>
<span data-ttu-id="40004-140">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40004-140">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="40004-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40004-141">-Confirm</span></span>
<span data-ttu-id="40004-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40004-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40004-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40004-143">-WhatIf</span></span>
<span data-ttu-id="40004-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40004-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40004-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40004-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40004-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40004-146">CommonParameters</span></span>
<span data-ttu-id="40004-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40004-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40004-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40004-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40004-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40004-149">INPUTS</span></span>

### <span data-ttu-id="40004-150">System. String</span><span class="sxs-lookup"><span data-stu-id="40004-150">System.String</span></span>

## <span data-ttu-id="40004-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40004-151">OUTPUTS</span></span>

### <span data-ttu-id="40004-152">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="40004-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="40004-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40004-153">NOTES</span></span>

## <span data-ttu-id="40004-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40004-154">RELATED LINKS</span></span>

[<span data-ttu-id="40004-155">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="40004-155">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="40004-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="40004-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="40004-157">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="40004-157">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


