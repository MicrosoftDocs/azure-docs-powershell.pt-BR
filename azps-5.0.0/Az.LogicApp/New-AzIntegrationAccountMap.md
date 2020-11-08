---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: a7803d95c2991dd829053a6d508432931701a220
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126087"
---
# <span data-ttu-id="343ca-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="343ca-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="343ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="343ca-102">SYNOPSIS</span></span>
<span data-ttu-id="343ca-103">Cria um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-103">Creates an integration account map.</span></span>

## <span data-ttu-id="343ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="343ca-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="343ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="343ca-105">DESCRIPTION</span></span>
<span data-ttu-id="343ca-106">O cmdlet **New-AzIntegrationAccountMap** cria um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="343ca-107">Esse cmdlet retorna um objeto que representa o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="343ca-108">Especificando o nome da conta de integração, o nome do grupo de recursos, o nome do mapa e a definição do mapa.</span><span class="sxs-lookup"><span data-stu-id="343ca-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="343ca-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="343ca-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="343ca-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="343ca-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="343ca-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="343ca-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="343ca-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="343ca-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="343ca-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="343ca-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="343ca-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="343ca-114">EXAMPLES</span></span>

### <span data-ttu-id="343ca-115">Exemplo 1: criar um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="343ca-115">Example 1: Create an integration account map</span></span>
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

<span data-ttu-id="343ca-116">Esse comando cria o mapa da conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="343ca-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="343ca-117">O comando especifica uma definição de mapa armazenada na variável $MapContent por um comando anterior.</span><span class="sxs-lookup"><span data-stu-id="343ca-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="343ca-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="343ca-118">Example 2</span></span>

<span data-ttu-id="343ca-119">Cria um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-119">Creates an integration account map.</span></span> <span data-ttu-id="343ca-120">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="343ca-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="343ca-121">OS</span><span class="sxs-lookup"><span data-stu-id="343ca-121">PARAMETERS</span></span>

### <span data-ttu-id="343ca-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="343ca-122">-ContentType</span></span>
<span data-ttu-id="343ca-123">Especifica um tipo de conteúdo para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="343ca-124">Esse cmdlet dá suporte a Application/XML como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="343ca-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="343ca-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="343ca-125">-DefaultProfile</span></span>
<span data-ttu-id="343ca-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="343ca-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="343ca-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="343ca-127">-MapDefinition</span></span>
<span data-ttu-id="343ca-128">Especifica um objeto de definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="343ca-129">Especifique esse parâmetro ou o parâmetro *MapFilePath* .</span><span class="sxs-lookup"><span data-stu-id="343ca-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="343ca-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="343ca-130">-MapFilePath</span></span>
<span data-ttu-id="343ca-131">Especifica o caminho do arquivo de uma definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="343ca-132">Especifique esse parâmetro ou o parâmetro *MapDefinition* .</span><span class="sxs-lookup"><span data-stu-id="343ca-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="343ca-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="343ca-133">-MapName</span></span>
<span data-ttu-id="343ca-134">Especifica um nome para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="343ca-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="343ca-135">-MapType</span></span>
<span data-ttu-id="343ca-136">Especifica o tipo do mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="343ca-137">Esse cmdlet dá suporte a XSLT como um tipo de mapa.</span><span class="sxs-lookup"><span data-stu-id="343ca-137">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="343ca-138">-Metadados</span><span class="sxs-lookup"><span data-stu-id="343ca-138">-Metadata</span></span>
<span data-ttu-id="343ca-139">Especifica um objeto de metadados para o mapa.</span><span class="sxs-lookup"><span data-stu-id="343ca-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="343ca-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="343ca-140">-Name</span></span>
<span data-ttu-id="343ca-141">Especifica um nome para a conta de integração.</span><span class="sxs-lookup"><span data-stu-id="343ca-141">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="343ca-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="343ca-142">-ResourceGroupName</span></span>
<span data-ttu-id="343ca-143">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="343ca-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="343ca-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="343ca-144">-Confirm</span></span>
<span data-ttu-id="343ca-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="343ca-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="343ca-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="343ca-146">-WhatIf</span></span>
<span data-ttu-id="343ca-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="343ca-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="343ca-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="343ca-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="343ca-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="343ca-149">CommonParameters</span></span>
<span data-ttu-id="343ca-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="343ca-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="343ca-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="343ca-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="343ca-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="343ca-152">INPUTS</span></span>

### <span data-ttu-id="343ca-153">System. String</span><span class="sxs-lookup"><span data-stu-id="343ca-153">System.String</span></span>

## <span data-ttu-id="343ca-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="343ca-154">OUTPUTS</span></span>

### <span data-ttu-id="343ca-155">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="343ca-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="343ca-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="343ca-156">NOTES</span></span>

## <span data-ttu-id="343ca-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="343ca-157">RELATED LINKS</span></span>

[<span data-ttu-id="343ca-158">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="343ca-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="343ca-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="343ca-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="343ca-160">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="343ca-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


