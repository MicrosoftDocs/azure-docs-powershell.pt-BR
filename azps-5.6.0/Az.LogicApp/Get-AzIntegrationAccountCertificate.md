---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: caf016d1e1ad18aee1904e9b69ae9330a5f34557
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886463"
---
# <span data-ttu-id="9528c-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9528c-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="9528c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9528c-102">SYNOPSIS</span></span>
<span data-ttu-id="9528c-103">Obtém certificados de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9528c-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="9528c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9528c-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9528c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9528c-105">DESCRIPTION</span></span>
<span data-ttu-id="9528c-106">O cmdlet **Get-AzIntegrationAccountCertificate** obtém certificados de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9528c-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="9528c-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="9528c-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="9528c-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="9528c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9528c-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="9528c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9528c-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9528c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9528c-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="9528c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9528c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9528c-112">EXAMPLES</span></span>

### <span data-ttu-id="9528c-113">Exemplo 1: obter um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="9528c-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="9528c-114">Este comando obtém o certificado de conta de integração chamado IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="9528c-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="9528c-115">Exemplo 2: Obter certificados de conta de integração pelo nome da conta de integração</span><span class="sxs-lookup"><span data-stu-id="9528c-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="9528c-116">Este comando obtém os certificados de conta de integração para a conta de integração chamada IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="9528c-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="9528c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9528c-117">PARAMETERS</span></span>

### <span data-ttu-id="9528c-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9528c-118">-CertificateName</span></span>
<span data-ttu-id="9528c-119">Especifica o nome de um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="9528c-119">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9528c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9528c-120">-DefaultProfile</span></span>
<span data-ttu-id="9528c-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9528c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9528c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9528c-122">-Name</span></span>
<span data-ttu-id="9528c-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="9528c-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9528c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9528c-124">-ResourceGroupName</span></span>
<span data-ttu-id="9528c-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9528c-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9528c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9528c-126">CommonParameters</span></span>
<span data-ttu-id="9528c-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9528c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9528c-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9528c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9528c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9528c-129">INPUTS</span></span>

### <span data-ttu-id="9528c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9528c-130">System.String</span></span>

## <span data-ttu-id="9528c-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9528c-131">OUTPUTS</span></span>

### <span data-ttu-id="9528c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9528c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="9528c-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="9528c-133">NOTES</span></span>

## <span data-ttu-id="9528c-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9528c-134">RELATED LINKS</span></span>

[<span data-ttu-id="9528c-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9528c-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="9528c-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9528c-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="9528c-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="9528c-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


