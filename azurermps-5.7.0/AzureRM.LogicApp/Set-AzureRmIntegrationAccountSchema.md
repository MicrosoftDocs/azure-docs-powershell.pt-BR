---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: e9981f32422f51910d7e1467f4da0b0c44118f24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610937"
---
# <span data-ttu-id="8191d-101">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8191d-101">Set-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="8191d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8191d-102">SYNOPSIS</span></span>
<span data-ttu-id="8191d-103">Modifica um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8191d-103">Modifies an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8191d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8191d-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8191d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8191d-105">DESCRIPTION</span></span>
<span data-ttu-id="8191d-106">O cmdlet **set-AzureRmIntegrationAccountSchema** modifica um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8191d-106">The **Set-AzureRmIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="8191d-107">Esse cmdlet retorna um objeto que representa o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8191d-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="8191d-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="8191d-108">Specify the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="8191d-109">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="8191d-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="8191d-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="8191d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8191d-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="8191d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8191d-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8191d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8191d-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="8191d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8191d-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8191d-114">EXAMPLES</span></span>

### <span data-ttu-id="8191d-115">Exemplo 1: modificar um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="8191d-115">Example 1: Modify an integration account schema</span></span>
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

<span data-ttu-id="8191d-116">Esse comando modifica o esquema da conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="8191d-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="8191d-117">OS</span><span class="sxs-lookup"><span data-stu-id="8191d-117">PARAMETERS</span></span>

### <span data-ttu-id="8191d-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="8191d-118">-ContentType</span></span>
<span data-ttu-id="8191d-119">Especifica um tipo de conteúdo para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8191d-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="8191d-120">Esse cmdlet dá suporte a Application/XML como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="8191d-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8191d-121">-DefaultProfile</span></span>
<span data-ttu-id="8191d-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8191d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8191d-123">-Force</span></span>
<span data-ttu-id="8191d-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8191d-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-125">-Metadados</span><span class="sxs-lookup"><span data-stu-id="8191d-125">-Metadata</span></span>
<span data-ttu-id="8191d-126">Especifica um objeto de metadados para o esquema.</span><span class="sxs-lookup"><span data-stu-id="8191d-126">Specifies a metadata object for the schema.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="8191d-127">-Name</span></span>
<span data-ttu-id="8191d-128">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8191d-128">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8191d-129">-ResourceGroupName</span></span>
<span data-ttu-id="8191d-130">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8191d-130">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="8191d-131">-SchemaDefinition</span></span>
<span data-ttu-id="8191d-132">Especifica um objeto de definição para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8191d-132">Specifies a definition object for integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="8191d-133">-SchemaFilePath</span></span>
<span data-ttu-id="8191d-134">Especifica o caminho do arquivo de uma definição para o esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8191d-134">Specifies the file path of a definition for the integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8191d-135">-SchemaName</span></span>
<span data-ttu-id="8191d-136">Especifica o nome do esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8191d-136">Specifies the name of the integration account schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="8191d-137">-SchemaType</span></span>
<span data-ttu-id="8191d-138">Especifica o tipo do esquema da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="8191d-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="8191d-139">Esse parâmetro dá suporte a XML como o tipo.</span><span class="sxs-lookup"><span data-stu-id="8191d-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8191d-140">-Confirm</span></span>
<span data-ttu-id="8191d-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8191d-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8191d-142">-WhatIf</span></span>
<span data-ttu-id="8191d-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8191d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8191d-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8191d-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8191d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8191d-145">CommonParameters</span></span>
<span data-ttu-id="8191d-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8191d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8191d-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8191d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8191d-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8191d-148">INPUTS</span></span>

### <span data-ttu-id="8191d-149">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8191d-149">None</span></span>
<span data-ttu-id="8191d-150">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8191d-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8191d-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8191d-151">OUTPUTS</span></span>

### <span data-ttu-id="8191d-152">Microsoft. Azure. Management. Logic. Models. IntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8191d-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="8191d-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8191d-153">NOTES</span></span>

## <span data-ttu-id="8191d-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8191d-154">RELATED LINKS</span></span>

[<span data-ttu-id="8191d-155">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8191d-155">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="8191d-156">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8191d-156">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="8191d-157">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="8191d-157">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)


