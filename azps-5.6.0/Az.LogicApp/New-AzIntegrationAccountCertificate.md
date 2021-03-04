---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 8b1da3fda8c8c016dd9cbe039015553f9073a4b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892753"
---
# <span data-ttu-id="bec8b-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bec8b-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="bec8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec8b-102">SYNOPSIS</span></span>
<span data-ttu-id="bec8b-103">Cria um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="bec8b-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="bec8b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bec8b-104">SYNTAX</span></span>

### <span data-ttu-id="bec8b-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="bec8b-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec8b-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="bec8b-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bec8b-107">Ambos</span><span class="sxs-lookup"><span data-stu-id="bec8b-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bec8b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bec8b-108">DESCRIPTION</span></span>
<span data-ttu-id="bec8b-109">O cmdlet **New-AzIntegrationAccountCertificate** cria um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="bec8b-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="bec8b-110">Este cmdlet retorna um objeto que representa o certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="bec8b-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="bec8b-111">Especifique o nome da conta de integração, o nome do grupo de recursos, o nome do certificado, o nome da chave, a versão da chave e a ID do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="bec8b-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="bec8b-112">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores de parâmetro de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="bec8b-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="bec8b-113">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="bec8b-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bec8b-114">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="bec8b-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bec8b-115">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bec8b-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bec8b-116">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="bec8b-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bec8b-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bec8b-117">EXAMPLES</span></span>

### <span data-ttu-id="bec8b-118">Exemplo 1: Criar um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="bec8b-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="bec8b-119">Este comando cria o certificado de conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="bec8b-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="bec8b-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bec8b-120">PARAMETERS</span></span>

### <span data-ttu-id="bec8b-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="bec8b-121">-CertificateName</span></span>
<span data-ttu-id="bec8b-122">Especifica um nome para o certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="bec8b-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="bec8b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec8b-123">-DefaultProfile</span></span>
<span data-ttu-id="bec8b-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="bec8b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bec8b-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="bec8b-125">-KeyName</span></span>
<span data-ttu-id="bec8b-126">Especifica o nome da chave do certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="bec8b-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8b-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="bec8b-127">-KeyVaultId</span></span>
<span data-ttu-id="bec8b-128">Especifica uma ID do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="bec8b-128">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8b-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="bec8b-129">-KeyVersion</span></span>
<span data-ttu-id="bec8b-130">Especifica a versão da chave de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="bec8b-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec8b-131">-Metadados</span><span class="sxs-lookup"><span data-stu-id="bec8b-131">-Metadata</span></span>
<span data-ttu-id="bec8b-132">Especifica um objeto de metadados para o certificado.</span><span class="sxs-lookup"><span data-stu-id="bec8b-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="bec8b-133">-Name</span><span class="sxs-lookup"><span data-stu-id="bec8b-133">-Name</span></span>
<span data-ttu-id="bec8b-134">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="bec8b-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="bec8b-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="bec8b-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="bec8b-136">Especifica o caminho de um arquivo de certificado público (.cer).</span><span class="sxs-lookup"><span data-stu-id="bec8b-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bec8b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec8b-137">-ResourceGroupName</span></span>
<span data-ttu-id="bec8b-138">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bec8b-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bec8b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bec8b-139">-Confirm</span></span>
<span data-ttu-id="bec8b-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bec8b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec8b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec8b-141">-WhatIf</span></span>
<span data-ttu-id="bec8b-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bec8b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec8b-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bec8b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec8b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec8b-144">CommonParameters</span></span>
<span data-ttu-id="bec8b-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec8b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec8b-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec8b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec8b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bec8b-147">INPUTS</span></span>

### <span data-ttu-id="bec8b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="bec8b-148">System.String</span></span>

## <span data-ttu-id="bec8b-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bec8b-149">OUTPUTS</span></span>

### <span data-ttu-id="bec8b-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bec8b-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="bec8b-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="bec8b-151">NOTES</span></span>

## <span data-ttu-id="bec8b-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bec8b-152">RELATED LINKS</span></span>

[<span data-ttu-id="bec8b-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bec8b-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="bec8b-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bec8b-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="bec8b-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bec8b-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


