---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: f9a332aaf50f60940391a52549d6f5549c77198b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116986"
---
# <span data-ttu-id="6df3c-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6df3c-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="6df3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6df3c-102">SYNOPSIS</span></span>
<span data-ttu-id="6df3c-103">Cria uma conexão automação.</span><span class="sxs-lookup"><span data-stu-id="6df3c-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="6df3c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6df3c-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6df3c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6df3c-105">DESCRIPTION</span></span>
<span data-ttu-id="6df3c-106">O **cmdlet New-AzAutomationConnection cria** uma conexão no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6df3c-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="6df3c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6df3c-107">EXAMPLES</span></span>

### <span data-ttu-id="6df3c-108">Exemplo 1: Criar uma conexão para ConnectionTypeName=Azure</span><span class="sxs-lookup"><span data-stu-id="6df3c-108">Example 1: Create a connection for ConnectionTypeName=Azure</span></span>
```
PS C:\> $FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6df3c-109">O primeiro comando atribui uma tabela hash de valores de campo à variável $FieldValue dados.</span><span class="sxs-lookup"><span data-stu-id="6df3c-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="6df3c-110">O segundo comando cria uma conexão do Azure chamada Conexão12 na conta automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="6df3c-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="6df3c-111">O comando usa os valores do campo de conexão $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="6df3c-111">The command uses the connection field values in $FieldValues.</span></span>

### <span data-ttu-id="6df3c-112">Exemplo 2: Criar uma conexão para ConnectionTypeName=AzureServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="6df3c-112">Example 2: Create a connection for ConnectionTypeName=AzureServicePrincipal</span></span>
```
PS C:\> $Thumbprint = "0SZTNJ34TCCMUJ5MJZGR8XQD3S0RVHJBA33Z8ZXV"
PS C:\> $TenantId = "4cd76576-b611-43d0-8f2b-adcb139531bf"
PS C:\> $ApplicationId = "3794a65a-e4e4-493d-ac1d-f04308d712dd"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $RunAsAccountConnectionFieldValues = @{"ApplicationId" = $ApplicationId; "TenantId" = $TenantId; "CertificateThumbprint" = $Thumbprint; "SubscriptionId" = $SubscriptionId}
PS C:\> New-AzAutomationConnection -Name "Connection13" -ConnectionTypeName AzureServicePrincipal -ConnectionFieldValues $RunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6df3c-113">O comando cria uma conexão do Azure chamada Conexão13 na conta automação chamada AutomationAccount01 usando $RunAsAccountConnectionFieldValues e ConnectionTypeName=AzureServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="6df3c-113">The command creates an Azure connection named Connection13 in the Automation account named AutomationAccount01 using $RunAsAccountConnectionFieldValues and ConnectionTypeName=AzureServicePrincipal.</span></span>
<span data-ttu-id="6df3c-114">Este ConnectionTypeName=AzureServicePrincipal é usado principalmente para o Azure Run As Account.</span><span class="sxs-lookup"><span data-stu-id="6df3c-114">This ConnectionTypeName=AzureServicePrincipal is mainly used for Azure Run As Account.</span></span>

### <span data-ttu-id="6df3c-115">Exemplo 3: Criar uma conexão para ConnectionTypeName=AzureClassicCertificate</span><span class="sxs-lookup"><span data-stu-id="6df3c-115">Example 3: Create a connection for ConnectionTypeName=AzureClassicCertificate</span></span>
```
PS C:\> $SubscriptionName = "MyTestSubscription"
PS C:\> $SubscriptionId = "81b59010-dc55-45b7-89cd-5ca26db62472"
PS C:\> $ClassicRunAsAccountCertifcateAssetName = "AzureClassicRunAsCertificate"
PS C:\> $ClassicRunAsAccountConnectionFieldValues = @{"SubscriptionName" = $SubscriptionName; "SubscriptionId" = $SubscriptionId; "CertificateAssetName" = $ClassicRunAsAccountCertifcateAssetName}
PS C:\> New-AzAutomationConnection -Name "Connection14" -ConnectionTypeName AzureClassicCertificate  -ConnectionFieldValues $ClassicRunAsAccountConnectionFieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="6df3c-116">O comando cria uma conexão do Azure chamada Conexão14 na conta automação chamada AutomationAccount01 usando $ClassicRunAsAccountConnectionFieldValues e ConnectionTypeName=AzureClassicCertificate.</span><span class="sxs-lookup"><span data-stu-id="6df3c-116">The command creates an Azure connection named Connection14 in the Automation account named AutomationAccount01 using $ClassicRunAsAccountConnectionFieldValues and ConnectionTypeName=AzureClassicCertificate.</span></span>
<span data-ttu-id="6df3c-117">Este ConnectionTypeName=AzureClassicCertificate é usado principalmente para o Azure Classic Run As Account.</span><span class="sxs-lookup"><span data-stu-id="6df3c-117">This ConnectionTypeName=AzureClassicCertificate is mainly used for Azure Classic Run As Account.</span></span>

## <span data-ttu-id="6df3c-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6df3c-118">PARAMETERS</span></span>

### <span data-ttu-id="6df3c-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6df3c-119">-AutomationAccountName</span></span>
<span data-ttu-id="6df3c-120">Especifica o nome da conta automação para a qual este cmdlet cria uma conexão.</span><span class="sxs-lookup"><span data-stu-id="6df3c-120">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="6df3c-121">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="6df3c-121">-ConnectionFieldValues</span></span>
<span data-ttu-id="6df3c-122">Especifica uma tabela hash que contém pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="6df3c-122">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="6df3c-123">As teclas representam os campos de conexão para o tipo de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="6df3c-123">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="6df3c-124">Os valores representam os valores específicos de cada campo de conexão para a instância de conexão.</span><span class="sxs-lookup"><span data-stu-id="6df3c-124">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="6df3c-125">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="6df3c-125">-ConnectionTypeName</span></span>
<span data-ttu-id="6df3c-126">Especifica o nome do tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="6df3c-126">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="6df3c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6df3c-127">-DefaultProfile</span></span>
<span data-ttu-id="6df3c-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6df3c-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6df3c-129">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6df3c-129">-Description</span></span>
<span data-ttu-id="6df3c-130">Especifica uma descrição para a conexão.</span><span class="sxs-lookup"><span data-stu-id="6df3c-130">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="6df3c-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="6df3c-131">-Name</span></span>
<span data-ttu-id="6df3c-132">Especifica um nome para a conexão.</span><span class="sxs-lookup"><span data-stu-id="6df3c-132">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="6df3c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df3c-133">-ResourceGroupName</span></span>
<span data-ttu-id="6df3c-134">Especifica o nome do grupo de recursos para o qual este cmdlet cria uma conexão.</span><span class="sxs-lookup"><span data-stu-id="6df3c-134">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="6df3c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df3c-135">CommonParameters</span></span>
<span data-ttu-id="6df3c-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6df3c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df3c-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df3c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df3c-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="6df3c-138">INPUTS</span></span>

### <span data-ttu-id="6df3c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="6df3c-139">System.String</span></span>

### <span data-ttu-id="6df3c-140">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="6df3c-140">System.Collections.IDictionary</span></span>

## <span data-ttu-id="6df3c-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="6df3c-141">OUTPUTS</span></span>

### <span data-ttu-id="6df3c-142">Microsoft.Azure.Commands.Automation.Model.Connection</span><span class="sxs-lookup"><span data-stu-id="6df3c-142">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="6df3c-143">Notas</span><span class="sxs-lookup"><span data-stu-id="6df3c-143">NOTES</span></span>

## <span data-ttu-id="6df3c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6df3c-144">RELATED LINKS</span></span>

[<span data-ttu-id="6df3c-145">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6df3c-145">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="6df3c-146">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="6df3c-146">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


