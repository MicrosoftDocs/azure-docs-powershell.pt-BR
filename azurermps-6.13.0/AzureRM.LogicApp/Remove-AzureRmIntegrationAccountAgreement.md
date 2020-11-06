---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 2eca24fadd72234639e46e7298f9fe5ada2766f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440774"
---
# <span data-ttu-id="60c4f-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="60c4f-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="60c4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="60c4f-103">Remove um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="60c4f-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60c4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60c4f-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60c4f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60c4f-105">DESCRIPTION</span></span>
<span data-ttu-id="60c4f-106">O cmdlet **Remove-AzureRmIntegrationAccountAgreement** remove um contrato de conta de integração de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="60c4f-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="60c4f-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="60c4f-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="60c4f-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="60c4f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="60c4f-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="60c4f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="60c4f-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="60c4f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="60c4f-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="60c4f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="60c4f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60c4f-112">EXAMPLES</span></span>

### <span data-ttu-id="60c4f-113">Exemplo 1: remover um contrato de conta de integração por nome</span><span class="sxs-lookup"><span data-stu-id="60c4f-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="60c4f-114">Esse comando Remove o contrato da conta de integração chamado IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="60c4f-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="60c4f-115">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="60c4f-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="60c4f-116">OS</span><span class="sxs-lookup"><span data-stu-id="60c4f-116">PARAMETERS</span></span>

### <span data-ttu-id="60c4f-117">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="60c4f-117">-AgreementName</span></span>
<span data-ttu-id="60c4f-118">Especifica o nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="60c4f-118">Specifies the name of the integration account agreement.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c4f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c4f-119">-DefaultProfile</span></span>
<span data-ttu-id="60c4f-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="60c4f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60c4f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="60c4f-121">-Force</span></span>
<span data-ttu-id="60c4f-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="60c4f-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="60c4f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="60c4f-123">-Name</span></span>
<span data-ttu-id="60c4f-124">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="60c4f-124">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c4f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c4f-125">-ResourceGroupName</span></span>
<span data-ttu-id="60c4f-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60c4f-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="60c4f-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60c4f-127">-Confirm</span></span>
<span data-ttu-id="60c4f-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60c4f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60c4f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60c4f-129">-WhatIf</span></span>
<span data-ttu-id="60c4f-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60c4f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60c4f-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60c4f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60c4f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c4f-132">CommonParameters</span></span>
<span data-ttu-id="60c4f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c4f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c4f-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c4f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c4f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60c4f-135">INPUTS</span></span>

### <span data-ttu-id="60c4f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="60c4f-136">System.String</span></span>

## <span data-ttu-id="60c4f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60c4f-137">OUTPUTS</span></span>

### <span data-ttu-id="60c4f-138">System. void</span><span class="sxs-lookup"><span data-stu-id="60c4f-138">System.Void</span></span>

## <span data-ttu-id="60c4f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60c4f-139">NOTES</span></span>

## <span data-ttu-id="60c4f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60c4f-140">RELATED LINKS</span></span>

[<span data-ttu-id="60c4f-141">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="60c4f-141">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="60c4f-142">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="60c4f-142">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="60c4f-143">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="60c4f-143">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


