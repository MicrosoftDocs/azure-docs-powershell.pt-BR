---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: cedd95d235abc6e114359de63dfbf1f4e58f26c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440620"
---
# <span data-ttu-id="ee5d5-101">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ee5d5-101">Set-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="ee5d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5d5-103">Modifica um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-103">Modifies an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee5d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee5d5-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee5d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee5d5-105">DESCRIPTION</span></span>
<span data-ttu-id="ee5d5-106">O cmdlet **set-AzureRmIntegrationAccountSchema** modifica um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-106">The **Set-AzureRmIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="ee5d5-107">Esse cmdlet retorna um objeto que representa o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="ee5d5-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-108">Specify the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="ee5d5-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="ee5d5-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ee5d5-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ee5d5-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ee5d5-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ee5d5-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee5d5-114">EXAMPLES</span></span>

### <span data-ttu-id="ee5d5-115">Exemplo 1: modificar um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="ee5d5-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
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

<span data-ttu-id="ee5d5-116">Esse comando modifica o esquema da conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="ee5d5-117">OS</span><span class="sxs-lookup"><span data-stu-id="ee5d5-117">PARAMETERS</span></span>

### <span data-ttu-id="ee5d5-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="ee5d5-118">-ContentType</span></span>
<span data-ttu-id="ee5d5-119">Especifica um tipo de conteúdo para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="ee5d5-120">Esse cmdlet dá suporte a Application/XML como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="ee5d5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ee5d5-121">-Force</span></span>
<span data-ttu-id="ee5d5-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ee5d5-123">-Metadados</span><span class="sxs-lookup"><span data-stu-id="ee5d5-123">-Metadata</span></span>
<span data-ttu-id="ee5d5-124">Especifica um objeto de metadados para o esquema.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-124">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="ee5d5-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee5d5-125">-Name</span></span>
<span data-ttu-id="ee5d5-126">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-126">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="ee5d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="ee5d5-128">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ee5d5-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="ee5d5-129">-SchemaDefinition</span></span>
<span data-ttu-id="ee5d5-130">Especifica um objeto de definição para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-130">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="ee5d5-131">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="ee5d5-131">-SchemaFilePath</span></span>
<span data-ttu-id="ee5d5-132">Especifica o caminho do arquivo de uma definição para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-132">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="ee5d5-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ee5d5-133">-SchemaName</span></span>
<span data-ttu-id="ee5d5-134">Especifica o nome do esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-134">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="ee5d5-135">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="ee5d5-135">-SchemaType</span></span>
<span data-ttu-id="ee5d5-136">Especifica o tipo do esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-136">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="ee5d5-137">Esse parâmetro dá suporte a XML como o tipo.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-137">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="ee5d5-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ee5d5-138">-Confirm</span></span>
<span data-ttu-id="ee5d5-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee5d5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee5d5-140">-WhatIf</span></span>
<span data-ttu-id="ee5d5-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee5d5-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee5d5-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5d5-143">-DefaultProfile</span></span>
<span data-ttu-id="ee5d5-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee5d5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5d5-145">CommonParameters</span></span>
<span data-ttu-id="ee5d5-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee5d5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5d5-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee5d5-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5d5-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee5d5-148">INPUTS</span></span>

## <span data-ttu-id="ee5d5-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee5d5-149">OUTPUTS</span></span>

### <span data-ttu-id="ee5d5-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ee5d5-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="ee5d5-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee5d5-151">NOTES</span></span>

## <span data-ttu-id="ee5d5-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee5d5-152">RELATED LINKS</span></span>

[<span data-ttu-id="ee5d5-153">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ee5d5-153">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="ee5d5-154">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ee5d5-154">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="ee5d5-155">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="ee5d5-155">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)


