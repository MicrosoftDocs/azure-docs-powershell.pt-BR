---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111823"
---
# <span data-ttu-id="54e85-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="54e85-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="54e85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54e85-102">SYNOPSIS</span></span>
<span data-ttu-id="54e85-103">Remove um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="54e85-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="54e85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54e85-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54e85-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54e85-105">DESCRIPTION</span></span>
<span data-ttu-id="54e85-106">O cmdlet **Remove-AzIntegrationAccountAgreement** remove um contrato de conta de integração de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="54e85-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="54e85-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="54e85-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="54e85-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="54e85-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="54e85-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="54e85-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="54e85-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="54e85-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="54e85-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="54e85-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="54e85-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54e85-112">EXAMPLES</span></span>

### <span data-ttu-id="54e85-113">Exemplo 1: remover um contrato de conta de integração por nome</span><span class="sxs-lookup"><span data-stu-id="54e85-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="54e85-114">Esse comando Remove o contrato da conta de integração chamado IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="54e85-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="54e85-115">O comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="54e85-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="54e85-116">OS</span><span class="sxs-lookup"><span data-stu-id="54e85-116">PARAMETERS</span></span>

### <span data-ttu-id="54e85-117">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="54e85-117">-AgreementName</span></span>
<span data-ttu-id="54e85-118">Especifica o nome do contrato da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="54e85-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="54e85-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e85-119">-DefaultProfile</span></span>
<span data-ttu-id="54e85-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="54e85-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54e85-121">-Force</span><span class="sxs-lookup"><span data-stu-id="54e85-121">-Force</span></span>
<span data-ttu-id="54e85-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="54e85-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54e85-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="54e85-123">-Name</span></span>
<span data-ttu-id="54e85-124">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="54e85-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="54e85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54e85-125">-ResourceGroupName</span></span>
<span data-ttu-id="54e85-126">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="54e85-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="54e85-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54e85-127">-Confirm</span></span>
<span data-ttu-id="54e85-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54e85-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54e85-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54e85-129">-WhatIf</span></span>
<span data-ttu-id="54e85-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54e85-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54e85-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54e85-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54e85-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e85-132">CommonParameters</span></span>
<span data-ttu-id="54e85-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54e85-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e85-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54e85-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e85-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54e85-135">INPUTS</span></span>

### <span data-ttu-id="54e85-136">System. String</span><span class="sxs-lookup"><span data-stu-id="54e85-136">System.String</span></span>

## <span data-ttu-id="54e85-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54e85-137">OUTPUTS</span></span>

### <span data-ttu-id="54e85-138">System. void</span><span class="sxs-lookup"><span data-stu-id="54e85-138">System.Void</span></span>

## <span data-ttu-id="54e85-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54e85-139">NOTES</span></span>

## <span data-ttu-id="54e85-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54e85-140">RELATED LINKS</span></span>

[<span data-ttu-id="54e85-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="54e85-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="54e85-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="54e85-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="54e85-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="54e85-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


