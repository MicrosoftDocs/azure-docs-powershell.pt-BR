---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: f6e1d4d987ece31a91d119d1fe2ab781475fdc94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886631"
---
# <span data-ttu-id="09533-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="09533-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="09533-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09533-102">SYNOPSIS</span></span>
<span data-ttu-id="09533-103">Remove um certificado de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09533-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="09533-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="09533-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09533-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="09533-105">DESCRIPTION</span></span>
<span data-ttu-id="09533-106">O cmdlet **Remove-AzIntegrationAccountCertificate** remove um certificado de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09533-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="09533-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="09533-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="09533-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="09533-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="09533-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="09533-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="09533-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="09533-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="09533-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="09533-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="09533-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09533-112">EXAMPLES</span></span>

### <span data-ttu-id="09533-113">Exemplo 1: Remover um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="09533-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="09533-114">Este comando remove o certificado de conta de integração chamado IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="09533-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="09533-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="09533-115">PARAMETERS</span></span>

### <span data-ttu-id="09533-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="09533-116">-CertificateName</span></span>
<span data-ttu-id="09533-117">Especifica o nome de um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="09533-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="09533-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09533-118">-DefaultProfile</span></span>
<span data-ttu-id="09533-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="09533-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09533-120">-Force</span><span class="sxs-lookup"><span data-stu-id="09533-120">-Force</span></span>
<span data-ttu-id="09533-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="09533-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09533-122">-Name</span><span class="sxs-lookup"><span data-stu-id="09533-122">-Name</span></span>
<span data-ttu-id="09533-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="09533-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="09533-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09533-124">-ResourceGroupName</span></span>
<span data-ttu-id="09533-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09533-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09533-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09533-126">-Confirm</span></span>
<span data-ttu-id="09533-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09533-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09533-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09533-128">-WhatIf</span></span>
<span data-ttu-id="09533-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09533-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09533-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09533-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09533-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09533-131">CommonParameters</span></span>
<span data-ttu-id="09533-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09533-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09533-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09533-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09533-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09533-134">INPUTS</span></span>

### <span data-ttu-id="09533-135">System.String</span><span class="sxs-lookup"><span data-stu-id="09533-135">System.String</span></span>

## <span data-ttu-id="09533-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="09533-136">OUTPUTS</span></span>

### <span data-ttu-id="09533-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="09533-137">System.Void</span></span>

## <span data-ttu-id="09533-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="09533-138">NOTES</span></span>

## <span data-ttu-id="09533-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09533-139">RELATED LINKS</span></span>

[<span data-ttu-id="09533-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="09533-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="09533-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="09533-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="09533-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="09533-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


