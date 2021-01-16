---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264562"
---
# <span data-ttu-id="3128f-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3128f-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="3128f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3128f-102">SYNOPSIS</span></span>
<span data-ttu-id="3128f-103">Cria uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="3128f-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="3128f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3128f-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3128f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3128f-105">DESCRIPTION</span></span>
<span data-ttu-id="3128f-106">O cmdlet **New-AzAutomationConnection** cria uma conexão na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3128f-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="3128f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3128f-107">EXAMPLES</span></span>

### <span data-ttu-id="3128f-108">Exemplo 1: criar uma conexão para ConnectionName = Azure</span><span class="sxs-lookup"><span data-stu-id="3128f-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="3128f-109">O primeiro comando atribui uma tabela de hash de valores de campo à variável $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="3128f-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="3128f-110">O segundo comando cria uma conexão do Azure chamada Connection12 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="3128f-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="3128f-111">O comando usa os valores do campo de conexão em $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="3128f-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="3128f-112">Exemplo 2: criar uma conexão para ConnectionName = AzureServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3128f-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="3128f-113">O comando cria uma conexão do Azure chamada Connection13 na conta de automação chamada AutomationAccount01 usando $RunAsAccountConnectionFieldValues e ConnectionName = AzureServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="3128f-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="3128f-114">Esse ConnectionName = AzureServicePrincipal é usado principalmente para a conta Executar como do Azure.</span><span class="sxs-lookup"><span data-stu-id="3128f-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="3128f-115">Exemplo 3: criar uma conexão para ConnectionName = AzureClassicCertificate</span><span class="sxs-lookup"><span data-stu-id="3128f-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="3128f-116">O comando cria uma conexão do Azure chamada Connection14 na conta de automação chamada AutomationAccount01 usando $ClassicRunAsAccountConnectionFieldValues e ConnectionName = AzureClassicCertificate.</span><span class="sxs-lookup"><span data-stu-id="3128f-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="3128f-117">Esse ConnectionName = AzureClassicCertificate é usado principalmente para a conta Executar como do Azure Classic.</span><span class="sxs-lookup"><span data-stu-id="3128f-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="3128f-118">OS</span><span class="sxs-lookup"><span data-stu-id="3128f-118">PARAMETERS</span></span>

### <span data-ttu-id="3128f-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3128f-119">-AutomationAccountName</span></span>
<span data-ttu-id="3128f-120">Especifica o nome da conta de automação para a qual esse cmdlet cria uma conexão.</span><span class="sxs-lookup"><span data-stu-id="3128f-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3128f-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="3128f-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="3128f-122">Especifica uma tabela de hash que contém pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="3128f-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="3128f-123">As chaves representam os campos de conexão do tipo de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="3128f-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="3128f-124">Os valores representam os valores específicos de cada campo de conexão para a instância de conexão.</span><span class="sxs-lookup"><span data-stu-id="3128f-124">The values represent the specific values of each connection field for the connection instance.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3128f-125">-ConnectionName</span><span class="sxs-lookup"><span data-stu-id="3128f-125">-ConnectionTypeName</span></span>
<span data-ttu-id="3128f-126">Especifica o nome do tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="3128f-126">Specifies the name of the connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3128f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3128f-127">-DefaultProfile</span></span>
<span data-ttu-id="3128f-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3128f-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3128f-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3128f-129">-Description</span></span>
<span data-ttu-id="3128f-130">Especifica uma descrição para a conexão.</span><span class="sxs-lookup"><span data-stu-id="3128f-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="3128f-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="3128f-131">-Name</span></span>
<span data-ttu-id="3128f-132">Especifica um nome para a conexão.</span><span class="sxs-lookup"><span data-stu-id="3128f-132">Specifies a name for the connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3128f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3128f-133">-ResourceGroupName</span></span>
<span data-ttu-id="3128f-134">Especifica o nome do grupo de recursos para o qual esse cmdlet cria uma conexão.</span><span class="sxs-lookup"><span data-stu-id="3128f-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3128f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3128f-135">CommonParameters</span></span>
<span data-ttu-id="3128f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3128f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3128f-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3128f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3128f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3128f-138">INPUTS</span></span>

### <span data-ttu-id="3128f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3128f-139">System.String</span></span>

### <span data-ttu-id="3128f-140">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="3128f-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="3128f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3128f-141">OUTPUTS</span></span>

### <span data-ttu-id="3128f-142">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="3128f-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="3128f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3128f-143">NOTES</span></span>

## <span data-ttu-id="3128f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3128f-144">RELATED LINKS</span></span>

[<span data-ttu-id="3128f-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3128f-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="3128f-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3128f-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


