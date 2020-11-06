---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 6291dbae1b03ff362424278987c454affa041b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440781"
---
# <span data-ttu-id="677ea-101">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="677ea-101">New-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="677ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="677ea-102">SYNOPSIS</span></span>
<span data-ttu-id="677ea-103">Cria um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="677ea-103">Creates an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="677ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="677ea-104">SYNTAX</span></span>

### <span data-ttu-id="677ea-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="677ea-105">PrivateKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="677ea-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="677ea-106">PublicKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="677ea-107">Simultaneamente</span><span class="sxs-lookup"><span data-stu-id="677ea-107">Both</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="677ea-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="677ea-108">DESCRIPTION</span></span>
<span data-ttu-id="677ea-109">O cmdlet **New-AzureRmIntegrationAccountCertificate** cria um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="677ea-109">The **New-AzureRmIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="677ea-110">Esse cmdlet retorna um objeto que representa o certificado da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="677ea-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="677ea-111">Especifique o nome da conta de integração, o nome do grupo de recursos, o nome do certificado, o nome da chave, versão da chave e a ID do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="677ea-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="677ea-112">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="677ea-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="677ea-113">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="677ea-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="677ea-114">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="677ea-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="677ea-115">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="677ea-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="677ea-116">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="677ea-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="677ea-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="677ea-117">EXAMPLES</span></span>

### <span data-ttu-id="677ea-118">Exemplo 1: criar um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="677ea-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="677ea-119">Esse comando cria o certificado da conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="677ea-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="677ea-120">OS</span><span class="sxs-lookup"><span data-stu-id="677ea-120">PARAMETERS</span></span>

### <span data-ttu-id="677ea-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="677ea-121">-CertificateName</span></span>
<span data-ttu-id="677ea-122">Especifica um nome para o certificado da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="677ea-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="677ea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="677ea-123">-DefaultProfile</span></span>
<span data-ttu-id="677ea-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="677ea-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="677ea-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="677ea-125">-KeyName</span></span>
<span data-ttu-id="677ea-126">Especifica o nome da chave de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="677ea-126">Specifies the name of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="677ea-127">-Keyvaultid</span><span class="sxs-lookup"><span data-stu-id="677ea-127">-KeyVaultId</span></span>
<span data-ttu-id="677ea-128">Especifica uma ID do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="677ea-128">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="677ea-129">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="677ea-129">-KeyVersion</span></span>
<span data-ttu-id="677ea-130">Especifica a versão da chave de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="677ea-130">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="677ea-131">-Metadados</span><span class="sxs-lookup"><span data-stu-id="677ea-131">-Metadata</span></span>
<span data-ttu-id="677ea-132">Especifica um objeto de metadados para o certificado.</span><span class="sxs-lookup"><span data-stu-id="677ea-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="677ea-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="677ea-133">-Name</span></span>
<span data-ttu-id="677ea-134">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="677ea-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="677ea-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="677ea-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="677ea-136">Especifica o caminho de um arquivo de certificado público (. cer).</span><span class="sxs-lookup"><span data-stu-id="677ea-136">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="677ea-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="677ea-137">-ResourceGroupName</span></span>
<span data-ttu-id="677ea-138">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="677ea-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="677ea-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="677ea-139">-Confirm</span></span>
<span data-ttu-id="677ea-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="677ea-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="677ea-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="677ea-141">-WhatIf</span></span>
<span data-ttu-id="677ea-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="677ea-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="677ea-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="677ea-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="677ea-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="677ea-144">CommonParameters</span></span>
<span data-ttu-id="677ea-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="677ea-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="677ea-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="677ea-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="677ea-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="677ea-147">INPUTS</span></span>

### <span data-ttu-id="677ea-148">System. String</span><span class="sxs-lookup"><span data-stu-id="677ea-148">System.String</span></span>

## <span data-ttu-id="677ea-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="677ea-149">OUTPUTS</span></span>

### <span data-ttu-id="677ea-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="677ea-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="677ea-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="677ea-151">NOTES</span></span>

## <span data-ttu-id="677ea-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="677ea-152">RELATED LINKS</span></span>

[<span data-ttu-id="677ea-153">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="677ea-153">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="677ea-154">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="677ea-154">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="677ea-155">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="677ea-155">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


