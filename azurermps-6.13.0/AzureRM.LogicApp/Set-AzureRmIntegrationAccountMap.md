---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 331f2d4c7bba584f5989cd724a3e25abaedfa5c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610310"
---
# <span data-ttu-id="73a7e-101">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="73a7e-101">Set-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="73a7e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="73a7e-103">Modifica um mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73a7e-103">Modifies an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73a7e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73a7e-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73a7e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73a7e-105">DESCRIPTION</span></span>
<span data-ttu-id="73a7e-106">O cmdlet **set-AzureRmIntegrationAccountMap** modifica um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73a7e-106">The **Set-AzureRmIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="73a7e-107">Esse cmdlet retorna um objeto que representa o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73a7e-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="73a7e-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do mapa.</span><span class="sxs-lookup"><span data-stu-id="73a7e-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="73a7e-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="73a7e-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="73a7e-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="73a7e-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="73a7e-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="73a7e-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="73a7e-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="73a7e-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="73a7e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73a7e-113">EXAMPLES</span></span>

### <span data-ttu-id="73a7e-114">Exemplo 1: modificar um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="73a7e-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="73a7e-115">Esse comando modifica o mapa da conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="73a7e-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="73a7e-116">O comando especifica uma definição de mapa armazenada na variável $MapContent por um comando anterior.</span><span class="sxs-lookup"><span data-stu-id="73a7e-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="73a7e-117">OS</span><span class="sxs-lookup"><span data-stu-id="73a7e-117">PARAMETERS</span></span>

### <span data-ttu-id="73a7e-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="73a7e-118">-ContentType</span></span>
<span data-ttu-id="73a7e-119">Especifica um tipo de conteúdo para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73a7e-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="73a7e-120">Esse cmdlet dá suporte a Application/XML como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="73a7e-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="73a7e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a7e-121">-DefaultProfile</span></span>
<span data-ttu-id="73a7e-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="73a7e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73a7e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="73a7e-123">-Force</span></span>
<span data-ttu-id="73a7e-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="73a7e-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="73a7e-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="73a7e-125">-MapDefinition</span></span>
<span data-ttu-id="73a7e-126">Especifica um objeto de definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73a7e-126">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="73a7e-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="73a7e-127">-MapFilePath</span></span>
<span data-ttu-id="73a7e-128">Especifica o caminho do arquivo de uma definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73a7e-128">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="73a7e-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="73a7e-129">-MapName</span></span>
<span data-ttu-id="73a7e-130">Especifica o nome de um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73a7e-130">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="73a7e-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="73a7e-131">-MapType</span></span>
<span data-ttu-id="73a7e-132">Especifica o tipo do mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73a7e-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="73a7e-133">Esse cmdlet dá suporte a XSLT como um tipo de mapa.</span><span class="sxs-lookup"><span data-stu-id="73a7e-133">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73a7e-134">-Metadados</span><span class="sxs-lookup"><span data-stu-id="73a7e-134">-Metadata</span></span>
<span data-ttu-id="73a7e-135">Especifica um objeto de metadados para o mapa.</span><span class="sxs-lookup"><span data-stu-id="73a7e-135">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="73a7e-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="73a7e-136">-Name</span></span>
<span data-ttu-id="73a7e-137">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73a7e-137">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="73a7e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a7e-138">-ResourceGroupName</span></span>
<span data-ttu-id="73a7e-139">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73a7e-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="73a7e-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="73a7e-140">-Confirm</span></span>
<span data-ttu-id="73a7e-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73a7e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a7e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a7e-142">-WhatIf</span></span>
<span data-ttu-id="73a7e-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73a7e-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73a7e-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73a7e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73a7e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a7e-145">CommonParameters</span></span>
<span data-ttu-id="73a7e-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a7e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a7e-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a7e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a7e-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73a7e-148">INPUTS</span></span>

### <span data-ttu-id="73a7e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="73a7e-149">System.String</span></span>

## <span data-ttu-id="73a7e-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73a7e-150">OUTPUTS</span></span>

### <span data-ttu-id="73a7e-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="73a7e-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="73a7e-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73a7e-152">NOTES</span></span>

## <span data-ttu-id="73a7e-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73a7e-153">RELATED LINKS</span></span>

[<span data-ttu-id="73a7e-154">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="73a7e-154">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="73a7e-155">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="73a7e-155">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="73a7e-156">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="73a7e-156">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)


