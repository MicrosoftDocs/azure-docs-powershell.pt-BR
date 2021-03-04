---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: 7ce86f893cbead5b2c5ac7a57af44eeb7f92f9ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886222"
---
# <span data-ttu-id="1b81c-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1b81c-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="1b81c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b81c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b81c-103">Cria um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-103">Creates an integration account map.</span></span>

## <span data-ttu-id="1b81c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1b81c-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b81c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1b81c-105">DESCRIPTION</span></span>
<span data-ttu-id="1b81c-106">O cmdlet **New-AzIntegrationAccountMap** cria um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="1b81c-107">Este cmdlet retorna um objeto que representa o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="1b81c-108">Especificando o nome da conta de integração, o nome do grupo de recursos, o nome do mapa e a definição do mapa.</span><span class="sxs-lookup"><span data-stu-id="1b81c-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="1b81c-109">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores de parâmetro de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="1b81c-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="1b81c-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="1b81c-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1b81c-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="1b81c-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1b81c-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1b81c-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1b81c-113">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="1b81c-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1b81c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b81c-114">EXAMPLES</span></span>

### <span data-ttu-id="1b81c-115">Exemplo 1: Criar um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="1b81c-115">Example 1: Create an integration account map</span></span>
```powershell
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

<span data-ttu-id="1b81c-116">Este comando cria o mapa da conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="1b81c-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="1b81c-117">O comando especifica uma definição de mapa armazenada na variável $MapContent por um comando anterior.</span><span class="sxs-lookup"><span data-stu-id="1b81c-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="1b81c-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1b81c-118">Example 2</span></span>

<span data-ttu-id="1b81c-119">Cria um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-119">Creates an integration account map.</span></span> <span data-ttu-id="1b81c-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="1b81c-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="1b81c-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1b81c-121">PARAMETERS</span></span>

### <span data-ttu-id="1b81c-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="1b81c-122">-ContentType</span></span>
<span data-ttu-id="1b81c-123">Especifica um tipo de conteúdo para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="1b81c-124">Este cmdlet dá suporte a aplicativo/xml como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="1b81c-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="1b81c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b81c-125">-DefaultProfile</span></span>
<span data-ttu-id="1b81c-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1b81c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b81c-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="1b81c-127">-MapDefinition</span></span>
<span data-ttu-id="1b81c-128">Especifica um objeto de definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="1b81c-129">Especifique esse parâmetro ou o *parâmetro MapFilePath.*</span><span class="sxs-lookup"><span data-stu-id="1b81c-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="1b81c-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="1b81c-130">-MapFilePath</span></span>
<span data-ttu-id="1b81c-131">Especifica o caminho do arquivo de uma definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="1b81c-132">Especifique esse parâmetro ou o *parâmetro MapDefinition.*</span><span class="sxs-lookup"><span data-stu-id="1b81c-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="1b81c-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="1b81c-133">-MapName</span></span>
<span data-ttu-id="1b81c-134">Especifica um nome para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="1b81c-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="1b81c-135">-MapType</span></span>
<span data-ttu-id="1b81c-136">Especifica o tipo do mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="1b81c-137">Este cmdlet dá suporte a Xslt como um tipo de mapa.</span><span class="sxs-lookup"><span data-stu-id="1b81c-137">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="1b81c-138">-Metadados</span><span class="sxs-lookup"><span data-stu-id="1b81c-138">-Metadata</span></span>
<span data-ttu-id="1b81c-139">Especifica um objeto de metadados para o mapa.</span><span class="sxs-lookup"><span data-stu-id="1b81c-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="1b81c-140">-Name</span><span class="sxs-lookup"><span data-stu-id="1b81c-140">-Name</span></span>
<span data-ttu-id="1b81c-141">Especifica um nome para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1b81c-141">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="1b81c-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b81c-142">-ResourceGroupName</span></span>
<span data-ttu-id="1b81c-143">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1b81c-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1b81c-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b81c-144">-Confirm</span></span>
<span data-ttu-id="1b81c-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b81c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b81c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b81c-146">-WhatIf</span></span>
<span data-ttu-id="1b81c-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b81c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b81c-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b81c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b81c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b81c-149">CommonParameters</span></span>
<span data-ttu-id="1b81c-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b81c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b81c-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b81c-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b81c-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b81c-152">INPUTS</span></span>

### <span data-ttu-id="1b81c-153">System.String</span><span class="sxs-lookup"><span data-stu-id="1b81c-153">System.String</span></span>

## <span data-ttu-id="1b81c-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1b81c-154">OUTPUTS</span></span>

### <span data-ttu-id="1b81c-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1b81c-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="1b81c-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="1b81c-156">NOTES</span></span>

## <span data-ttu-id="1b81c-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b81c-157">RELATED LINKS</span></span>

[<span data-ttu-id="1b81c-158">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1b81c-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="1b81c-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1b81c-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="1b81c-160">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="1b81c-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


