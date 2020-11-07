---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 68264ac0e0346405ee43bfb5dc876d48be9b4d9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770551"
---
# <span data-ttu-id="3b831-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3b831-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="3b831-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b831-102">SYNOPSIS</span></span>
<span data-ttu-id="3b831-103">Obtém um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3b831-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="3b831-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b831-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b831-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b831-105">DESCRIPTION</span></span>
<span data-ttu-id="3b831-106">O cmdlet **Get-AzIntegrationAccountAgreement** Obtém um contrato de conta de integração de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b831-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="3b831-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do contrato.</span><span class="sxs-lookup"><span data-stu-id="3b831-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="3b831-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="3b831-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3b831-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="3b831-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3b831-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3b831-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3b831-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="3b831-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3b831-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b831-112">EXAMPLES</span></span>

### <span data-ttu-id="3b831-113">Exemplo 1: obter um contrato de conta de integração</span><span class="sxs-lookup"><span data-stu-id="3b831-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
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

<span data-ttu-id="3b831-114">Esse comando obtém um contrato de conta de integração chamado IntegrationAccountAgreement06.</span><span class="sxs-lookup"><span data-stu-id="3b831-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="3b831-115">Exemplo 2: obter contratos da conta de integração por nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3b831-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="3b831-116">Esse comando obtém os contratos da conta de integração por nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b831-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="3b831-117">OS</span><span class="sxs-lookup"><span data-stu-id="3b831-117">PARAMETERS</span></span>

### <span data-ttu-id="3b831-118">-Agreementname</span><span class="sxs-lookup"><span data-stu-id="3b831-118">-AgreementName</span></span>
<span data-ttu-id="3b831-119">Especifica o nome de um contrato de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3b831-119">Specifies the name of an integration account agreement.</span></span>

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

### <span data-ttu-id="3b831-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b831-120">-DefaultProfile</span></span>
<span data-ttu-id="3b831-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3b831-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b831-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b831-122">-Name</span></span>
<span data-ttu-id="3b831-123">Especifica o nome de uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="3b831-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3b831-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b831-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b831-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b831-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3b831-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b831-126">CommonParameters</span></span>
<span data-ttu-id="3b831-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b831-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b831-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b831-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b831-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b831-129">INPUTS</span></span>

### <span data-ttu-id="3b831-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3b831-130">System.String</span></span>

## <span data-ttu-id="3b831-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b831-131">OUTPUTS</span></span>

### <span data-ttu-id="3b831-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3b831-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="3b831-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b831-133">NOTES</span></span>

## <span data-ttu-id="3b831-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b831-134">RELATED LINKS</span></span>

[<span data-ttu-id="3b831-135">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3b831-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="3b831-136">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3b831-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="3b831-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="3b831-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


