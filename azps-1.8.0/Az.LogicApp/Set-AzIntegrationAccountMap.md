---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: e2a66eef93d2ed59f78e492cac7fa7fac4dd0244
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770468"
---
# <span data-ttu-id="58075-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="58075-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="58075-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58075-102">SYNOPSIS</span></span>
<span data-ttu-id="58075-103">Modifica um mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="58075-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="58075-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58075-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58075-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58075-105">DESCRIPTION</span></span>
<span data-ttu-id="58075-106">O cmdlet **set-AzIntegrationAccountMap** modifica um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="58075-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="58075-107">Esse cmdlet retorna um objeto que representa o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="58075-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="58075-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do mapa.</span><span class="sxs-lookup"><span data-stu-id="58075-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="58075-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="58075-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="58075-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="58075-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="58075-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="58075-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="58075-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="58075-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="58075-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58075-113">EXAMPLES</span></span>

### <span data-ttu-id="58075-114">Exemplo 1: modificar um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="58075-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="58075-115">Esse comando modifica o mapa da conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="58075-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="58075-116">O comando especifica uma definição de mapa armazenada na variável $MapContent por um comando anterior.</span><span class="sxs-lookup"><span data-stu-id="58075-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="58075-117">OS</span><span class="sxs-lookup"><span data-stu-id="58075-117">PARAMETERS</span></span>

### <span data-ttu-id="58075-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="58075-118">-ContentType</span></span>
<span data-ttu-id="58075-119">Especifica um tipo de conteúdo para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="58075-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="58075-120">Esse cmdlet dá suporte a Application/XML como um tipo de conteúdo de mapa.</span><span class="sxs-lookup"><span data-stu-id="58075-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="58075-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58075-121">-DefaultProfile</span></span>
<span data-ttu-id="58075-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="58075-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58075-123">-Force</span><span class="sxs-lookup"><span data-stu-id="58075-123">-Force</span></span>
<span data-ttu-id="58075-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="58075-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58075-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="58075-125">-MapDefinition</span></span>
<span data-ttu-id="58075-126">Especifica um objeto de definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="58075-126">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="58075-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="58075-127">-MapFilePath</span></span>
<span data-ttu-id="58075-128">Especifica o caminho do arquivo de uma definição para o mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="58075-128">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="58075-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="58075-129">-MapName</span></span>
<span data-ttu-id="58075-130">Especifica o nome de um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="58075-130">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="58075-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="58075-131">-MapType</span></span>
<span data-ttu-id="58075-132">Especifica o tipo do mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="58075-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="58075-133">Esse cmdlet dá suporte a XSLT como um tipo de mapa.</span><span class="sxs-lookup"><span data-stu-id="58075-133">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="58075-134">-Metadados</span><span class="sxs-lookup"><span data-stu-id="58075-134">-Metadata</span></span>
<span data-ttu-id="58075-135">Especifica um objeto de metadados para o mapa.</span><span class="sxs-lookup"><span data-stu-id="58075-135">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="58075-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="58075-136">-Name</span></span>
<span data-ttu-id="58075-137">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="58075-137">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="58075-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58075-138">-ResourceGroupName</span></span>
<span data-ttu-id="58075-139">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="58075-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="58075-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58075-140">-Confirm</span></span>
<span data-ttu-id="58075-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58075-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58075-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58075-142">-WhatIf</span></span>
<span data-ttu-id="58075-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="58075-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58075-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58075-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58075-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58075-145">CommonParameters</span></span>
<span data-ttu-id="58075-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58075-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58075-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58075-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58075-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58075-148">INPUTS</span></span>

### <span data-ttu-id="58075-149">System. String</span><span class="sxs-lookup"><span data-stu-id="58075-149">System.String</span></span>

## <span data-ttu-id="58075-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58075-150">OUTPUTS</span></span>

### <span data-ttu-id="58075-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="58075-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="58075-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58075-152">NOTES</span></span>

## <span data-ttu-id="58075-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58075-153">RELATED LINKS</span></span>

[<span data-ttu-id="58075-154">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="58075-154">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="58075-155">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="58075-155">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="58075-156">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="58075-156">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


