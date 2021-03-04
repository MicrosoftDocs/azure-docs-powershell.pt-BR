---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: f963a89e6220e8154c2ba958adca318036c53474
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887978"
---
# <span data-ttu-id="6bfde-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6bfde-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="6bfde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bfde-102">SYNOPSIS</span></span>
<span data-ttu-id="6bfde-103">Modifica um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="6bfde-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6bfde-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bfde-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6bfde-105">DESCRIPTION</span></span>
<span data-ttu-id="6bfde-106">O cmdlet **Set-AzIntegrationAccountMap** modifica um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="6bfde-107">Este cmdlet retorna um objeto que representa o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="6bfde-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do mapa.</span><span class="sxs-lookup"><span data-stu-id="6bfde-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="6bfde-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="6bfde-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6bfde-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="6bfde-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6bfde-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6bfde-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6bfde-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="6bfde-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6bfde-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6bfde-113">EXAMPLES</span></span>

### <span data-ttu-id="6bfde-114">Exemplo 1: Modificar um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="6bfde-114">Example 1: Modify an integration account map</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="6bfde-115">Este comando modifica o mapa da conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="6bfde-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="6bfde-116">O comando especifica uma definição de mapa armazenada na variável $MapContent por um comando anterior.</span><span class="sxs-lookup"><span data-stu-id="6bfde-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="6bfde-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6bfde-117">Example 2</span></span>

<span data-ttu-id="6bfde-118">Modifica um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-118">Modifies an integration account map.</span></span> <span data-ttu-id="6bfde-119">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="6bfde-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="6bfde-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6bfde-120">PARAMETERS</span></span>

### <span data-ttu-id="6bfde-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="6bfde-121">-ContentType</span></span>
<span data-ttu-id="6bfde-122">Especifica um tipo de conteúdo para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="6bfde-123">Este cmdlet dá suporte a aplicativo/xml como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="6bfde-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="6bfde-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bfde-124">-DefaultProfile</span></span>
<span data-ttu-id="6bfde-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6bfde-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bfde-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6bfde-126">-Force</span></span>
<span data-ttu-id="6bfde-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6bfde-127">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bfde-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="6bfde-128">-MapDefinition</span></span>
<span data-ttu-id="6bfde-129">Especifica um objeto de definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="6bfde-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="6bfde-130">-MapFilePath</span></span>
<span data-ttu-id="6bfde-131">Especifica o caminho do arquivo de uma definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="6bfde-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="6bfde-132">-MapName</span></span>
<span data-ttu-id="6bfde-133">Especifica o nome de um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="6bfde-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="6bfde-134">-MapType</span></span>
<span data-ttu-id="6bfde-135">Especifica o tipo do mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="6bfde-136">Este cmdlet dá suporte a Xslt como um tipo de mapa.</span><span class="sxs-lookup"><span data-stu-id="6bfde-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="6bfde-137">-Metadados</span><span class="sxs-lookup"><span data-stu-id="6bfde-137">-Metadata</span></span>
<span data-ttu-id="6bfde-138">Especifica um objeto de metadados para o mapa.</span><span class="sxs-lookup"><span data-stu-id="6bfde-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="6bfde-139">-Name</span><span class="sxs-lookup"><span data-stu-id="6bfde-139">-Name</span></span>
<span data-ttu-id="6bfde-140">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="6bfde-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="6bfde-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bfde-141">-ResourceGroupName</span></span>
<span data-ttu-id="6bfde-142">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6bfde-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6bfde-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bfde-143">-Confirm</span></span>
<span data-ttu-id="6bfde-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bfde-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bfde-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bfde-145">-WhatIf</span></span>
<span data-ttu-id="6bfde-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6bfde-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bfde-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6bfde-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bfde-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bfde-148">CommonParameters</span></span>
<span data-ttu-id="6bfde-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bfde-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bfde-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bfde-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bfde-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bfde-151">INPUTS</span></span>

### <span data-ttu-id="6bfde-152">System.String</span><span class="sxs-lookup"><span data-stu-id="6bfde-152">System.String</span></span>

## <span data-ttu-id="6bfde-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6bfde-153">OUTPUTS</span></span>

### <span data-ttu-id="6bfde-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6bfde-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="6bfde-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="6bfde-155">NOTES</span></span>

## <span data-ttu-id="6bfde-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6bfde-156">RELATED LINKS</span></span>

[<span data-ttu-id="6bfde-157">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6bfde-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="6bfde-158">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6bfde-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="6bfde-159">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="6bfde-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


