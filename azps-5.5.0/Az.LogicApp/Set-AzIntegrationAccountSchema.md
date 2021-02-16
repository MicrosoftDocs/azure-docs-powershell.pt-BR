---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: c43bfb5fd43df92d6b8d1674b4a856829b3258d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113606"
---
# <span data-ttu-id="8d806-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d806-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="8d806-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d806-102">SYNOPSIS</span></span>
<span data-ttu-id="8d806-103">Modifica um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8d806-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="8d806-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d806-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d806-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d806-105">DESCRIPTION</span></span>
<span data-ttu-id="8d806-106">O cmdlet **Set-AzIntegrationAccountSchema** modifica um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8d806-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="8d806-107">Esse cmdlet retorna um objeto que representa o esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8d806-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="8d806-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="8d806-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="8d806-109">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores dos parâmetros de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="8d806-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="8d806-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="8d806-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8d806-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="8d806-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8d806-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8d806-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8d806-113">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="8d806-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8d806-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8d806-114">EXAMPLES</span></span>

### <span data-ttu-id="8d806-115">Exemplo 1: Modificar um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="8d806-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="8d806-116">Esse comando modifica o esquema de conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="8d806-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="8d806-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d806-117">PARAMETERS</span></span>

### <span data-ttu-id="8d806-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="8d806-118">-ContentType</span></span>
<span data-ttu-id="8d806-119">Especifica um tipo de conteúdo para o esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8d806-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="8d806-120">Este cmdlet dá suporte a aplicativo/xml como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="8d806-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="8d806-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d806-121">-DefaultProfile</span></span>
<span data-ttu-id="8d806-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8d806-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d806-123">-Forçar</span><span class="sxs-lookup"><span data-stu-id="8d806-123">-Force</span></span>
<span data-ttu-id="8d806-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d806-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8d806-125">-Metadados</span><span class="sxs-lookup"><span data-stu-id="8d806-125">-Metadata</span></span>
<span data-ttu-id="8d806-126">Especifica um objeto de metadados para o esquema.</span><span class="sxs-lookup"><span data-stu-id="8d806-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="8d806-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d806-127">-Name</span></span>
<span data-ttu-id="8d806-128">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8d806-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="8d806-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d806-129">-ResourceGroupName</span></span>
<span data-ttu-id="8d806-130">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d806-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8d806-131">-EsquemaDefinition</span><span class="sxs-lookup"><span data-stu-id="8d806-131">-SchemaDefinition</span></span>
<span data-ttu-id="8d806-132">Especifica um objeto de definição para esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8d806-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="8d806-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="8d806-133">-SchemaFilePath</span></span>
<span data-ttu-id="8d806-134">Especifica o caminho do arquivo de uma definição para o esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8d806-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="8d806-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8d806-135">-SchemaName</span></span>
<span data-ttu-id="8d806-136">Especifica o nome do esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8d806-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="8d806-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="8d806-137">-SchemaType</span></span>
<span data-ttu-id="8d806-138">Especifica o tipo para o esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8d806-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="8d806-139">Esse parâmetro dá suporte a Xml como o tipo.</span><span class="sxs-lookup"><span data-stu-id="8d806-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d806-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8d806-140">-Confirm</span></span>
<span data-ttu-id="8d806-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d806-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d806-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d806-142">-WhatIf</span></span>
<span data-ttu-id="8d806-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8d806-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d806-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d806-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d806-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d806-145">CommonParameters</span></span>
<span data-ttu-id="8d806-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d806-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d806-147">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d806-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d806-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="8d806-148">INPUTS</span></span>

### <span data-ttu-id="8d806-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8d806-149">System.String</span></span>

## <span data-ttu-id="8d806-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="8d806-150">OUTPUTS</span></span>

### <span data-ttu-id="8d806-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d806-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="8d806-152">Notas</span><span class="sxs-lookup"><span data-stu-id="8d806-152">NOTES</span></span>

## <span data-ttu-id="8d806-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d806-153">RELATED LINKS</span></span>

[<span data-ttu-id="8d806-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d806-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="8d806-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d806-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="8d806-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8d806-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


