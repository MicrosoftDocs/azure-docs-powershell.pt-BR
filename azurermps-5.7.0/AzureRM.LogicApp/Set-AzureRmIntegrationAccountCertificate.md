---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: a0ffbc31727b7267be59b9645d99abdce1bfeae7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429754"
---
# <span data-ttu-id="596e4-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="596e4-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="596e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="596e4-102">SYNOPSIS</span></span>
<span data-ttu-id="596e4-103">Modifica um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="596e4-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="596e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="596e4-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="596e4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="596e4-105">DESCRIPTION</span></span>
<span data-ttu-id="596e4-106">O cmdlet **set-AzureRmIntegrationAccountCertificate** modifica um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="596e4-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="596e4-107">Esse cmdlet retorna um objeto que representa o certificado da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="596e4-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="596e4-108">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="596e4-108">Specifying the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="596e4-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="596e4-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="596e4-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="596e4-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="596e4-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="596e4-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="596e4-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="596e4-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="596e4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="596e4-113">EXAMPLES</span></span>

### <span data-ttu-id="596e4-114">Exemplo 1: modificar um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="596e4-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="596e4-115">Esse comando modifica o certificado da conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="596e4-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="596e4-116">OS</span><span class="sxs-lookup"><span data-stu-id="596e4-116">PARAMETERS</span></span>

### <span data-ttu-id="596e4-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="596e4-117">-CertificateName</span></span>
<span data-ttu-id="596e4-118">Especifica o nome de um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="596e4-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="596e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596e4-119">-DefaultProfile</span></span>
<span data-ttu-id="596e4-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="596e4-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="596e4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="596e4-121">-Force</span></span>
<span data-ttu-id="596e4-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="596e4-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="596e4-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="596e4-123">-KeyName</span></span>
<span data-ttu-id="596e4-124">Especifica o nome de uma chave de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="596e4-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596e4-125">-Keyvaultid</span><span class="sxs-lookup"><span data-stu-id="596e4-125">-KeyVaultId</span></span>
<span data-ttu-id="596e4-126">Especifica uma ID do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="596e4-126">Specifies a key vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596e4-127">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="596e4-127">-KeyVersion</span></span>
<span data-ttu-id="596e4-128">Especifica a versão da chave de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="596e4-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596e4-129">-Metadados</span><span class="sxs-lookup"><span data-stu-id="596e4-129">-Metadata</span></span>
<span data-ttu-id="596e4-130">Especifica um objeto de metadados para o certificado.</span><span class="sxs-lookup"><span data-stu-id="596e4-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="596e4-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="596e4-131">-Name</span></span>
<span data-ttu-id="596e4-132">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="596e4-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="596e4-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="596e4-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="596e4-134">Especifica o caminho de um arquivo de certificado público (. cer).</span><span class="sxs-lookup"><span data-stu-id="596e4-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596e4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="596e4-135">-ResourceGroupName</span></span>
<span data-ttu-id="596e4-136">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="596e4-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="596e4-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="596e4-137">-Confirm</span></span>
<span data-ttu-id="596e4-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="596e4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="596e4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="596e4-139">-WhatIf</span></span>
<span data-ttu-id="596e4-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="596e4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="596e4-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="596e4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="596e4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596e4-142">CommonParameters</span></span>
<span data-ttu-id="596e4-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596e4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596e4-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="596e4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596e4-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="596e4-145">INPUTS</span></span>

### <span data-ttu-id="596e4-146">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="596e4-146">None</span></span>
<span data-ttu-id="596e4-147">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="596e4-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="596e4-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="596e4-148">OUTPUTS</span></span>

### <span data-ttu-id="596e4-149">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="596e4-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="596e4-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="596e4-150">NOTES</span></span>

## <span data-ttu-id="596e4-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="596e4-151">RELATED LINKS</span></span>

[<span data-ttu-id="596e4-152">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="596e4-152">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="596e4-153">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="596e4-153">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="596e4-154">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="596e4-154">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)


