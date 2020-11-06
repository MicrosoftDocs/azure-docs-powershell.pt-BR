---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: eadd3052bb965b60bdaf377cd45fc014f25cac79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603273"
---
# <span data-ttu-id="bd11e-101">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bd11e-101">Get-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="bd11e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd11e-102">SYNOPSIS</span></span>
<span data-ttu-id="bd11e-103">Obtém um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="bd11e-103">Gets an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd11e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd11e-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd11e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd11e-105">DESCRIPTION</span></span>
<span data-ttu-id="bd11e-106">O cmdlet **Get-AzureRmIntegrationAccountAgreement** Obtém um contrato de conta de integração de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="bd11e-106">The **Get-AzureRmIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="bd11e-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="bd11e-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="bd11e-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="bd11e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bd11e-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="bd11e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bd11e-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bd11e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bd11e-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="bd11e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bd11e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd11e-112">EXAMPLES</span></span>

### <span data-ttu-id="bd11e-113">Exemplo 1: obter um contrato de conta de integração</span><span class="sxs-lookup"><span data-stu-id="bd11e-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="bd11e-114">Esse comando obtém um contrato de conta de integração chamado IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="bd11e-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="bd11e-115">Exemplo 2: obter contratos da conta de integração por nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bd11e-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="bd11e-116">Esse comando obtém os contratos da conta de integração por nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd11e-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="bd11e-117">OS</span><span class="sxs-lookup"><span data-stu-id="bd11e-117">PARAMETERS</span></span>

### <span data-ttu-id="bd11e-118">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="bd11e-118">-AgreementName</span></span>
<span data-ttu-id="bd11e-119">Especifica o nome de um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="bd11e-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="bd11e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd11e-120">-DefaultProfile</span></span>
<span data-ttu-id="bd11e-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bd11e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd11e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd11e-122">-Name</span></span>
<span data-ttu-id="bd11e-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="bd11e-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="bd11e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd11e-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd11e-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd11e-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bd11e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd11e-126">CommonParameters</span></span>
<span data-ttu-id="bd11e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd11e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd11e-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd11e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd11e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd11e-129">INPUTS</span></span>

### <span data-ttu-id="bd11e-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bd11e-130">None</span></span>
<span data-ttu-id="bd11e-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="bd11e-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd11e-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd11e-132">OUTPUTS</span></span>

### <span data-ttu-id="bd11e-133">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bd11e-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="bd11e-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd11e-134">NOTES</span></span>

## <span data-ttu-id="bd11e-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd11e-135">RELATED LINKS</span></span>

[<span data-ttu-id="bd11e-136">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bd11e-136">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="bd11e-137">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bd11e-137">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="bd11e-138">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bd11e-138">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


