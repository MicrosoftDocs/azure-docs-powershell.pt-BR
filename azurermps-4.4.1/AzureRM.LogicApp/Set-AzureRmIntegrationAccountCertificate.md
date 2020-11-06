---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: feb885ca6f08a7396fd88db73d48172dc002f055
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433093"
---
# <span data-ttu-id="e0e6f-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0e6f-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="e0e6f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e6f-103">Modifica um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0e6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0e6f-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0e6f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0e6f-105">DESCRIPTION</span></span>
<span data-ttu-id="e0e6f-106">O cmdlet **set-AzureRmIntegrationAccountCertificate** modifica um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="e0e6f-107">Esse cmdlet retorna um objeto que representa o certificado da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="e0e6f-108">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-108">Specifying the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="e0e6f-109">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e0e6f-110">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e0e6f-111">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e0e6f-112">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e0e6f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0e6f-113">EXAMPLES</span></span>

### <span data-ttu-id="e0e6f-114">Exemplo 1: modificar um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="e0e6f-114">Example 1: Modify an integration account certificate</span></span>
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

<span data-ttu-id="e0e6f-115">Esse comando modifica o certificado da conta de integração no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="e0e6f-116">OS</span><span class="sxs-lookup"><span data-stu-id="e0e6f-116">PARAMETERS</span></span>

### <span data-ttu-id="e0e6f-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e0e6f-117">-CertificateName</span></span>
<span data-ttu-id="e0e6f-118">Especifica o nome de um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="e0e6f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e0e6f-119">-Force</span></span>
<span data-ttu-id="e0e6f-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0e6f-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e0e6f-121">-KeyName</span></span>
<span data-ttu-id="e0e6f-122">Especifica o nome de uma chave de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-122">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="e0e6f-123">-Keyvaultid</span><span class="sxs-lookup"><span data-stu-id="e0e6f-123">-KeyVaultId</span></span>
<span data-ttu-id="e0e6f-124">Especifica uma ID do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-124">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="e0e6f-125">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="e0e6f-125">-KeyVersion</span></span>
<span data-ttu-id="e0e6f-126">Especifica a versão da chave de certificado no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-126">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="e0e6f-127">-Metadados</span><span class="sxs-lookup"><span data-stu-id="e0e6f-127">-Metadata</span></span>
<span data-ttu-id="e0e6f-128">Especifica um objeto de metadados para o certificado.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-128">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="e0e6f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0e6f-129">-Name</span></span>
<span data-ttu-id="e0e6f-130">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-130">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="e0e6f-131">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e0e6f-131">-PublicCertificateFilePath</span></span>
<span data-ttu-id="e0e6f-132">Especifica o caminho de um arquivo de certificado público (. cer).</span><span class="sxs-lookup"><span data-stu-id="e0e6f-132">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="e0e6f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0e6f-133">-ResourceGroupName</span></span>
<span data-ttu-id="e0e6f-134">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e0e6f-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0e6f-135">-Confirm</span></span>
<span data-ttu-id="e0e6f-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0e6f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0e6f-137">-WhatIf</span></span>
<span data-ttu-id="e0e6f-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0e6f-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0e6f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0e6f-140">-DefaultProfile</span></span>
<span data-ttu-id="e0e6f-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0e6f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e6f-142">CommonParameters</span></span>
<span data-ttu-id="e0e6f-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e6f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e6f-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e6f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e6f-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0e6f-145">INPUTS</span></span>

## <span data-ttu-id="e0e6f-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0e6f-146">OUTPUTS</span></span>

### <span data-ttu-id="e0e6f-147">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0e6f-147">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="e0e6f-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0e6f-148">NOTES</span></span>

## <span data-ttu-id="e0e6f-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0e6f-149">RELATED LINKS</span></span>

[<span data-ttu-id="e0e6f-150">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0e6f-150">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="e0e6f-151">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0e6f-151">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="e0e6f-152">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e0e6f-152">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)


