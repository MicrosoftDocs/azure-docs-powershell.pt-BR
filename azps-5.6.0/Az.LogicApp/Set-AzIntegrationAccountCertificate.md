---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: c7ae1404cfff2d725326b9f5a8f2b7244c030109
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891186"
---
# <span data-ttu-id="aa9b8-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9b8-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="aa9b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9b8-103">Modifica um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="aa9b8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aa9b8-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa9b8-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aa9b8-105">DESCRIPTION</span></span>
<span data-ttu-id="aa9b8-106">O cmdlet **Set-AzIntegrationAccountCertificate** modifica um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="aa9b8-107">Este cmdlet retorna um objeto que representa o certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="aa9b8-108">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="aa9b8-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="aa9b8-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="aa9b8-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="aa9b8-112">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="aa9b8-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa9b8-113">EXAMPLES</span></span>

### <span data-ttu-id="aa9b8-114">Exemplo 1: Modificar um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="aa9b8-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="aa9b8-115">Este comando modifica o certificado de conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="aa9b8-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aa9b8-116">PARAMETERS</span></span>

### <span data-ttu-id="aa9b8-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="aa9b8-117">-CertificateName</span></span>
<span data-ttu-id="aa9b8-118">Especifica o nome de um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="aa9b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa9b8-119">-DefaultProfile</span></span>
<span data-ttu-id="aa9b8-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="aa9b8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa9b8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="aa9b8-121">-Force</span></span>
<span data-ttu-id="aa9b8-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa9b8-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="aa9b8-123">-KeyName</span></span>
<span data-ttu-id="aa9b8-124">Especifica o nome de uma chave de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa9b8-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="aa9b8-125">-KeyVaultId</span></span>
<span data-ttu-id="aa9b8-126">Especifica uma ID do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-126">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa9b8-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="aa9b8-127">-KeyVersion</span></span>
<span data-ttu-id="aa9b8-128">Especifica a versão da chave de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa9b8-129">-Metadados</span><span class="sxs-lookup"><span data-stu-id="aa9b8-129">-Metadata</span></span>
<span data-ttu-id="aa9b8-130">Especifica um objeto de metadados para o certificado.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="aa9b8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="aa9b8-131">-Name</span></span>
<span data-ttu-id="aa9b8-132">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="aa9b8-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="aa9b8-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="aa9b8-134">Especifica o caminho de um arquivo de certificado público (.cer).</span><span class="sxs-lookup"><span data-stu-id="aa9b8-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa9b8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa9b8-135">-ResourceGroupName</span></span>
<span data-ttu-id="aa9b8-136">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="aa9b8-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa9b8-137">-Confirm</span></span>
<span data-ttu-id="aa9b8-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa9b8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa9b8-139">-WhatIf</span></span>
<span data-ttu-id="aa9b8-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa9b8-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa9b8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9b8-142">CommonParameters</span></span>
<span data-ttu-id="aa9b8-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa9b8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9b8-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa9b8-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9b8-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa9b8-145">INPUTS</span></span>

### <span data-ttu-id="aa9b8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="aa9b8-146">System.String</span></span>

## <span data-ttu-id="aa9b8-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aa9b8-147">OUTPUTS</span></span>

### <span data-ttu-id="aa9b8-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9b8-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="aa9b8-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="aa9b8-149">NOTES</span></span>

## <span data-ttu-id="aa9b8-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa9b8-150">RELATED LINKS</span></span>

[<span data-ttu-id="aa9b8-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9b8-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="aa9b8-152">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9b8-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="aa9b8-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="aa9b8-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


