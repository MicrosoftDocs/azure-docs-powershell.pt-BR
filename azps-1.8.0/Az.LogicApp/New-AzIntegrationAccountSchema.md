---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 23dd1ba36a634e1b1d49e4623a9c652cda5bab27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770500"
---
# <span data-ttu-id="3a261-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3a261-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="3a261-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3a261-102">SYNOPSIS</span></span>
<span data-ttu-id="3a261-103">Cria um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3a261-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="3a261-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3a261-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a261-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3a261-105">DESCRIPTION</span></span>
<span data-ttu-id="3a261-106">O cmdlet **New-AzIntegrationAccountSchema** cria um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3a261-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="3a261-107">Esse cmdlet retorna um objeto que representa o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3a261-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="3a261-108">Especifique o nome da conta de integração, o nome do grupo de recursos, o nome do esquema e a definição do esquema.</span><span class="sxs-lookup"><span data-stu-id="3a261-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="3a261-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="3a261-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="3a261-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="3a261-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3a261-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="3a261-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3a261-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3a261-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3a261-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="3a261-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3a261-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a261-114">EXAMPLES</span></span>

### <span data-ttu-id="3a261-115">Exemplo 1: criar o esquema da conta de integração</span><span class="sxs-lookup"><span data-stu-id="3a261-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="3a261-116">Esse comando cria o esquema da conta de integração chamado IntegrationAccountSchema1 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="3a261-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="3a261-117">OS</span><span class="sxs-lookup"><span data-stu-id="3a261-117">PARAMETERS</span></span>

### <span data-ttu-id="3a261-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="3a261-118">-ContentType</span></span>
<span data-ttu-id="3a261-119">Especifica um tipo de conteúdo para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3a261-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="3a261-120">Esse cmdlet dá suporte a Application/XML como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="3a261-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="3a261-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a261-121">-DefaultProfile</span></span>
<span data-ttu-id="3a261-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3a261-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a261-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="3a261-123">-Metadata</span></span>
<span data-ttu-id="3a261-124">Especifica um objeto de metadados para o esquema.</span><span class="sxs-lookup"><span data-stu-id="3a261-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="3a261-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a261-125">-Name</span></span>
<span data-ttu-id="3a261-126">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3a261-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3a261-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a261-127">-ResourceGroupName</span></span>
<span data-ttu-id="3a261-128">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3a261-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3a261-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="3a261-129">-SchemaDefinition</span></span>
<span data-ttu-id="3a261-130">Especifica um objeto de definição para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3a261-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="3a261-131">Especifique esse parâmetro ou o parâmetro *SchemaFilePath* .</span><span class="sxs-lookup"><span data-stu-id="3a261-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="3a261-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="3a261-132">-SchemaFilePath</span></span>
<span data-ttu-id="3a261-133">Especifica o caminho do arquivo de uma definição para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3a261-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="3a261-134">Especifique esse parâmetro ou o parâmetro *SchemaDefinition* .</span><span class="sxs-lookup"><span data-stu-id="3a261-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="3a261-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="3a261-135">-SchemaName</span></span>
<span data-ttu-id="3a261-136">Especifica um nome para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3a261-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="3a261-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="3a261-137">-SchemaType</span></span>
<span data-ttu-id="3a261-138">Especifica o tipo do esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3a261-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="3a261-139">Esse parâmetro dá suporte a XML como o tipo.</span><span class="sxs-lookup"><span data-stu-id="3a261-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="3a261-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3a261-140">-Confirm</span></span>
<span data-ttu-id="3a261-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a261-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a261-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a261-142">-WhatIf</span></span>
<span data-ttu-id="3a261-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a261-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a261-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a261-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a261-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a261-145">CommonParameters</span></span>
<span data-ttu-id="3a261-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a261-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a261-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a261-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a261-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3a261-148">INPUTS</span></span>

### <span data-ttu-id="3a261-149">System. String</span><span class="sxs-lookup"><span data-stu-id="3a261-149">System.String</span></span>

## <span data-ttu-id="3a261-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3a261-150">OUTPUTS</span></span>

### <span data-ttu-id="3a261-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3a261-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="3a261-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3a261-152">NOTES</span></span>

## <span data-ttu-id="3a261-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a261-153">RELATED LINKS</span></span>

[<span data-ttu-id="3a261-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3a261-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="3a261-155">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3a261-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="3a261-156">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="3a261-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


