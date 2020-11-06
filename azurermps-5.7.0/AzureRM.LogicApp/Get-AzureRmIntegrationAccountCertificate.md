---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 268dd2c54d9881281a5b1ee331a5b5d98892f7b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432480"
---
# <span data-ttu-id="73bde-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="73bde-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="73bde-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="73bde-102">SYNOPSIS</span></span>
<span data-ttu-id="73bde-103">Obtém certificados de conta de integração a partir de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73bde-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73bde-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73bde-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73bde-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="73bde-105">DESCRIPTION</span></span>
<span data-ttu-id="73bde-106">O cmdlet **Get-AzureRmIntegrationAccountCertificate** obtém certificados de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73bde-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="73bde-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do certificado.</span><span class="sxs-lookup"><span data-stu-id="73bde-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="73bde-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="73bde-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="73bde-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="73bde-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="73bde-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="73bde-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="73bde-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="73bde-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="73bde-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73bde-112">EXAMPLES</span></span>

### <span data-ttu-id="73bde-113">Exemplo 1: obter um certificado de conta de integração</span><span class="sxs-lookup"><span data-stu-id="73bde-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="73bde-114">Esse comando obtém o certificado da conta de integração chamado IntegrationAccountCertificate01.</span><span class="sxs-lookup"><span data-stu-id="73bde-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="73bde-115">Exemplo 2: obter certificados da conta de integração pelo nome da conta de integração</span><span class="sxs-lookup"><span data-stu-id="73bde-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="73bde-116">Esse comando obtém os certificados da conta de integração da conta de integração chamada IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="73bde-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="73bde-117">OS</span><span class="sxs-lookup"><span data-stu-id="73bde-117">PARAMETERS</span></span>

### <span data-ttu-id="73bde-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="73bde-118">-CertificateName</span></span>
<span data-ttu-id="73bde-119">Especifica o nome de um certificado de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73bde-119">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bde-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bde-120">-DefaultProfile</span></span>
<span data-ttu-id="73bde-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="73bde-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73bde-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="73bde-122">-Name</span></span>
<span data-ttu-id="73bde-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="73bde-123">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bde-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bde-124">-ResourceGroupName</span></span>
<span data-ttu-id="73bde-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="73bde-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="73bde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bde-126">CommonParameters</span></span>
<span data-ttu-id="73bde-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73bde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bde-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73bde-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bde-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="73bde-129">INPUTS</span></span>

### <span data-ttu-id="73bde-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="73bde-130">None</span></span>
<span data-ttu-id="73bde-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="73bde-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73bde-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="73bde-132">OUTPUTS</span></span>

### <span data-ttu-id="73bde-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="73bde-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="73bde-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="73bde-134">NOTES</span></span>

## <span data-ttu-id="73bde-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73bde-135">RELATED LINKS</span></span>

[<span data-ttu-id="73bde-136">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="73bde-136">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="73bde-137">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="73bde-137">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="73bde-138">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="73bde-138">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


