---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: e8bf71ec58273e89ad8f32e65c9c110205239dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440850"
---
# <span data-ttu-id="b900a-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b900a-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="b900a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b900a-102">SYNOPSIS</span></span>
<span data-ttu-id="b900a-103">Modifica um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b900a-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b900a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b900a-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b900a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b900a-105">DESCRIPTION</span></span>
<span data-ttu-id="b900a-106">O cmdlet **set-AzureRmIntegrationAccountPartner** modifica um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b900a-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="b900a-107">Esse cmdlet retorna um objeto que representa o parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b900a-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="b900a-108">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do parceiro.</span><span class="sxs-lookup"><span data-stu-id="b900a-108">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="b900a-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="b900a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b900a-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="b900a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b900a-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b900a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b900a-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="b900a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b900a-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b900a-113">EXAMPLES</span></span>

### <span data-ttu-id="b900a-114">Exemplo 1: modificar um parceiro de conta de integração</span><span class="sxs-lookup"><span data-stu-id="b900a-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="b900a-115">Esse comando modifica o parceiro da conta de integração chamado IntegrationAccountPartner22 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="b900a-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="b900a-116">OS</span><span class="sxs-lookup"><span data-stu-id="b900a-116">PARAMETERS</span></span>

### <span data-ttu-id="b900a-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="b900a-117">-BusinessIdentities</span></span>
<span data-ttu-id="b900a-118">Especifica as identidades comerciais para o parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b900a-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="b900a-119">Especifique uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b900a-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="b900a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b900a-120">-DefaultProfile</span></span>
<span data-ttu-id="b900a-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b900a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b900a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b900a-122">-Force</span></span>
<span data-ttu-id="b900a-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="b900a-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b900a-124">-Metadados</span><span class="sxs-lookup"><span data-stu-id="b900a-124">-Metadata</span></span>
<span data-ttu-id="b900a-125">Especifica um objeto de metadados para o parceiro.</span><span class="sxs-lookup"><span data-stu-id="b900a-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="b900a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="b900a-126">-Name</span></span>
<span data-ttu-id="b900a-127">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b900a-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b900a-128">-Partnername</span><span class="sxs-lookup"><span data-stu-id="b900a-128">-PartnerName</span></span>
<span data-ttu-id="b900a-129">Especifica o nome do parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b900a-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="b900a-130">-Partnertype</span><span class="sxs-lookup"><span data-stu-id="b900a-130">-PartnerType</span></span>
<span data-ttu-id="b900a-131">Especifica o tipo da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="b900a-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="b900a-132">Esse parâmetro dá suporte para o tipo B2B.</span><span class="sxs-lookup"><span data-stu-id="b900a-132">This parameter supports the type B2B.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b900a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b900a-133">-ResourceGroupName</span></span>
<span data-ttu-id="b900a-134">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b900a-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b900a-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b900a-135">-Confirm</span></span>
<span data-ttu-id="b900a-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b900a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b900a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b900a-137">-WhatIf</span></span>
<span data-ttu-id="b900a-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b900a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b900a-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b900a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b900a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b900a-140">CommonParameters</span></span>
<span data-ttu-id="b900a-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b900a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b900a-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b900a-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b900a-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b900a-143">INPUTS</span></span>

### <span data-ttu-id="b900a-144">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b900a-144">None</span></span>
<span data-ttu-id="b900a-145">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b900a-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b900a-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b900a-146">OUTPUTS</span></span>

### <span data-ttu-id="b900a-147">Microsoft. Azure. Management. Logic. Models. IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b900a-147">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="b900a-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b900a-148">NOTES</span></span>

## <span data-ttu-id="b900a-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b900a-149">RELATED LINKS</span></span>

[<span data-ttu-id="b900a-150">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b900a-150">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="b900a-151">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b900a-151">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="b900a-152">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b900a-152">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

