---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: 54012fbc157b18c4485200895fb7e68926dded07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770459"
---
# <span data-ttu-id="7b328-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7b328-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="7b328-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7b328-102">SYNOPSIS</span></span>
<span data-ttu-id="7b328-103">Modifica um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b328-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="7b328-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7b328-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b328-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7b328-105">DESCRIPTION</span></span>
<span data-ttu-id="7b328-106">O cmdlet **set-AzIntegrationAccountSchema** modifica um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b328-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="7b328-107">Esse cmdlet retorna um objeto que representa o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b328-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="7b328-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="7b328-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="7b328-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="7b328-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="7b328-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="7b328-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7b328-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="7b328-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7b328-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7b328-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7b328-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="7b328-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7b328-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b328-114">EXAMPLES</span></span>

### <span data-ttu-id="7b328-115">Exemplo 1: modificar um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="7b328-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="7b328-116">Esse comando modifica o esquema da conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="7b328-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="7b328-117">OS</span><span class="sxs-lookup"><span data-stu-id="7b328-117">PARAMETERS</span></span>

### <span data-ttu-id="7b328-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="7b328-118">-ContentType</span></span>
<span data-ttu-id="7b328-119">Especifica um tipo de conteúdo para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b328-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="7b328-120">Esse cmdlet dá suporte a Application/XML como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="7b328-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="7b328-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b328-121">-DefaultProfile</span></span>
<span data-ttu-id="7b328-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7b328-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b328-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7b328-123">-Force</span></span>
<span data-ttu-id="7b328-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7b328-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7b328-125">-Metadados</span><span class="sxs-lookup"><span data-stu-id="7b328-125">-Metadata</span></span>
<span data-ttu-id="7b328-126">Especifica um objeto de metadados para o esquema.</span><span class="sxs-lookup"><span data-stu-id="7b328-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="7b328-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="7b328-127">-Name</span></span>
<span data-ttu-id="7b328-128">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b328-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="7b328-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b328-129">-ResourceGroupName</span></span>
<span data-ttu-id="7b328-130">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7b328-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7b328-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="7b328-131">-SchemaDefinition</span></span>
<span data-ttu-id="7b328-132">Especifica um objeto de definição para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b328-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="7b328-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="7b328-133">-SchemaFilePath</span></span>
<span data-ttu-id="7b328-134">Especifica o caminho do arquivo de uma definição para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b328-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="7b328-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="7b328-135">-SchemaName</span></span>
<span data-ttu-id="7b328-136">Especifica o nome do esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b328-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="7b328-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="7b328-137">-SchemaType</span></span>
<span data-ttu-id="7b328-138">Especifica o tipo do esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="7b328-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="7b328-139">Esse parâmetro dá suporte a XML como o tipo.</span><span class="sxs-lookup"><span data-stu-id="7b328-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="7b328-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7b328-140">-Confirm</span></span>
<span data-ttu-id="7b328-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b328-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b328-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b328-142">-WhatIf</span></span>
<span data-ttu-id="7b328-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b328-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b328-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b328-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b328-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b328-145">CommonParameters</span></span>
<span data-ttu-id="7b328-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b328-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b328-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b328-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b328-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7b328-148">INPUTS</span></span>

### <span data-ttu-id="7b328-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7b328-149">System.String</span></span>

## <span data-ttu-id="7b328-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7b328-150">OUTPUTS</span></span>

### <span data-ttu-id="7b328-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7b328-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="7b328-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7b328-152">NOTES</span></span>

## <span data-ttu-id="7b328-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b328-153">RELATED LINKS</span></span>

[<span data-ttu-id="7b328-154">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7b328-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="7b328-155">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7b328-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="7b328-156">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7b328-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)


