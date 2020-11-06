---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 29eb57e7c076499f105bec9e2400091ac11b09fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428195"
---
# <span data-ttu-id="0376f-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0376f-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="0376f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0376f-102">SYNOPSIS</span></span>
<span data-ttu-id="0376f-103">Remove um parceiro de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0376f-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0376f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0376f-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0376f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0376f-105">DESCRIPTION</span></span>
<span data-ttu-id="0376f-106">O cmdlet **Remove-AzureRmIntegrationAccountPartner** remove um parceiro de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0376f-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="0376f-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do parceiro.</span><span class="sxs-lookup"><span data-stu-id="0376f-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="0376f-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="0376f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0376f-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="0376f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0376f-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0376f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0376f-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="0376f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0376f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0376f-112">EXAMPLES</span></span>

### <span data-ttu-id="0376f-113">Exemplo 1: remover um parceiro de conta de integração</span><span class="sxs-lookup"><span data-stu-id="0376f-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="0376f-114">Esse comando Remove o parceiro da conta de integração chamado IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="0376f-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="0376f-115">OS</span><span class="sxs-lookup"><span data-stu-id="0376f-115">PARAMETERS</span></span>

### <span data-ttu-id="0376f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0376f-116">-DefaultProfile</span></span>
<span data-ttu-id="0376f-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0376f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0376f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0376f-118">-Force</span></span>
<span data-ttu-id="0376f-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0376f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0376f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0376f-120">-Name</span></span>
<span data-ttu-id="0376f-121">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0376f-121">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0376f-122">-Partnername</span><span class="sxs-lookup"><span data-stu-id="0376f-122">-PartnerName</span></span>
<span data-ttu-id="0376f-123">Especifica o nome do parceiro da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="0376f-123">Specifies the name of the integration account partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0376f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0376f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0376f-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0376f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0376f-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0376f-126">-Confirm</span></span>
<span data-ttu-id="0376f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0376f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0376f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0376f-128">-WhatIf</span></span>
<span data-ttu-id="0376f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0376f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0376f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0376f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0376f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0376f-131">CommonParameters</span></span>
<span data-ttu-id="0376f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0376f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0376f-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0376f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0376f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0376f-134">INPUTS</span></span>

### <span data-ttu-id="0376f-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0376f-135">None</span></span>
<span data-ttu-id="0376f-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0376f-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0376f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0376f-137">OUTPUTS</span></span>

## <span data-ttu-id="0376f-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0376f-138">NOTES</span></span>

## <span data-ttu-id="0376f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0376f-139">RELATED LINKS</span></span>

[<span data-ttu-id="0376f-140">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0376f-140">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="0376f-141">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0376f-141">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="0376f-142">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="0376f-142">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


