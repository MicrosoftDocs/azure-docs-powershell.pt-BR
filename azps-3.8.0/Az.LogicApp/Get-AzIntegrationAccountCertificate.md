---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 46927e25fb4e32aae9ea1870ef9eeaedd5efe008
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777724"
---
# <span data-ttu-id="61c07-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="61c07-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="61c07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="61c07-102">SYNOPSIS</span></span>
<span data-ttu-id="61c07-103">Obtém certificados de conta de integração a partir de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61c07-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="61c07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61c07-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61c07-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="61c07-105">DESCRIPTION</span></span>
<span data-ttu-id="61c07-106">O cmdlet **Get-AzIntegrationAccountCertificate** obtém certificados de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61c07-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="61c07-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="61c07-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="61c07-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="61c07-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="61c07-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="61c07-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="61c07-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="61c07-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="61c07-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="61c07-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="61c07-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61c07-112">EXAMPLES</span></span>

### <span data-ttu-id="61c07-113">Exemplo 1: obter um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="61c07-113">Example 1: Get an integration account certificate</span></span>
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

<span data-ttu-id="61c07-114">Esse comando obtém o certificado da conta de integração chamado IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="61c07-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="61c07-115">Exemplo 2: obter certificados da conta de integração pelo nome da conta de integração</span><span class="sxs-lookup"><span data-stu-id="61c07-115">Example 2: Get integration account certificates by integration account name</span></span>
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

<span data-ttu-id="61c07-116">Esse comando obtém os certificados da conta de integração da conta de integração chamada IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="61c07-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="61c07-117">OS</span><span class="sxs-lookup"><span data-stu-id="61c07-117">PARAMETERS</span></span>

### <span data-ttu-id="61c07-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="61c07-118">-CertificateName</span></span>
<span data-ttu-id="61c07-119">Especifica o nome de um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="61c07-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="61c07-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61c07-120">-DefaultProfile</span></span>
<span data-ttu-id="61c07-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="61c07-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61c07-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="61c07-122">-Name</span></span>
<span data-ttu-id="61c07-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="61c07-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="61c07-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61c07-124">-ResourceGroupName</span></span>
<span data-ttu-id="61c07-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61c07-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="61c07-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61c07-126">CommonParameters</span></span>
<span data-ttu-id="61c07-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61c07-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61c07-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61c07-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61c07-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="61c07-129">INPUTS</span></span>

### <span data-ttu-id="61c07-130">System. String</span><span class="sxs-lookup"><span data-stu-id="61c07-130">System.String</span></span>

## <span data-ttu-id="61c07-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="61c07-131">OUTPUTS</span></span>

### <span data-ttu-id="61c07-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="61c07-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="61c07-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="61c07-133">NOTES</span></span>

## <span data-ttu-id="61c07-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61c07-134">RELATED LINKS</span></span>

[<span data-ttu-id="61c07-135">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="61c07-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="61c07-136">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="61c07-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="61c07-137">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="61c07-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


