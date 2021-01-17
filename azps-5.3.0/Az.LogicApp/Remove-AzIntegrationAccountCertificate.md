---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429201"
---
# <span data-ttu-id="1dd5a-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1dd5a-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="1dd5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1dd5a-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd5a-103">Remove um certificado de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="1dd5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1dd5a-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd5a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1dd5a-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd5a-106">O cmdlet **Remove-AzIntegrationAccountCertificate** remove um certificado de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="1dd5a-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="1dd5a-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1dd5a-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1dd5a-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1dd5a-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1dd5a-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1dd5a-112">EXAMPLES</span></span>

### <span data-ttu-id="1dd5a-113">Exemplo 1: remover um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="1dd5a-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="1dd5a-114">Esse comando Remove o certificado da conta de integração chamado IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="1dd5a-115">OS</span><span class="sxs-lookup"><span data-stu-id="1dd5a-115">PARAMETERS</span></span>

### <span data-ttu-id="1dd5a-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="1dd5a-116">-CertificateName</span></span>
<span data-ttu-id="1dd5a-117">Especifica o nome de um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="1dd5a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dd5a-118">-DefaultProfile</span></span>
<span data-ttu-id="1dd5a-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1dd5a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dd5a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="1dd5a-120">-Force</span></span>
<span data-ttu-id="1dd5a-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1dd5a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dd5a-122">-Name</span></span>
<span data-ttu-id="1dd5a-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="1dd5a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dd5a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1dd5a-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1dd5a-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1dd5a-126">-Confirm</span></span>
<span data-ttu-id="1dd5a-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dd5a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd5a-128">-WhatIf</span></span>
<span data-ttu-id="1dd5a-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dd5a-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dd5a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd5a-131">CommonParameters</span></span>
<span data-ttu-id="1dd5a-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd5a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd5a-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd5a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd5a-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1dd5a-134">INPUTS</span></span>

### <span data-ttu-id="1dd5a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1dd5a-135">System.String</span></span>

## <span data-ttu-id="1dd5a-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1dd5a-136">OUTPUTS</span></span>

### <span data-ttu-id="1dd5a-137">System. void</span><span class="sxs-lookup"><span data-stu-id="1dd5a-137">System.Void</span></span>

## <span data-ttu-id="1dd5a-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1dd5a-138">NOTES</span></span>

## <span data-ttu-id="1dd5a-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1dd5a-139">RELATED LINKS</span></span>

[<span data-ttu-id="1dd5a-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1dd5a-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1dd5a-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1dd5a-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1dd5a-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1dd5a-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


