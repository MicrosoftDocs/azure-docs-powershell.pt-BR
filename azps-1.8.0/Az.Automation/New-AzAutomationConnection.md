---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationConnection.md
ms.openlocfilehash: b1dffae1543e2c896dc8461048f94d5724c6dc00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601573"
---
# <span data-ttu-id="86c1c-101">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="86c1c-101">New-AzAutomationConnection</span></span>

## <span data-ttu-id="86c1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="86c1c-103">Cria uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="86c1c-103">Creates an Automation connection.</span></span>

## <span data-ttu-id="86c1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86c1c-104">SYNTAX</span></span>

```
New-AzAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86c1c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86c1c-105">DESCRIPTION</span></span>
<span data-ttu-id="86c1c-106">O cmdlet **New-AzAutomationConnection** cria uma conexão na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="86c1c-106">The **New-AzAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="86c1c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86c1c-107">EXAMPLES</span></span>

### <span data-ttu-id="86c1c-108">Exemplo 1: criar uma conexão</span><span class="sxs-lookup"><span data-stu-id="86c1c-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="86c1c-109">O primeiro comando atribui uma tabela de hash de valores de campo à variável $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="86c1c-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>
<span data-ttu-id="86c1c-110">O segundo comando cria uma conexão do Azure chamada Connection12 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="86c1c-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="86c1c-111">O comando usa os valores do campo de conexão em $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="86c1c-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="86c1c-112">OS</span><span class="sxs-lookup"><span data-stu-id="86c1c-112">PARAMETERS</span></span>

### <span data-ttu-id="86c1c-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="86c1c-113">-AutomationAccountName</span></span>
<span data-ttu-id="86c1c-114">Especifica o nome da conta de automação para a qual esse cmdlet cria uma conexão.</span><span class="sxs-lookup"><span data-stu-id="86c1c-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="86c1c-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="86c1c-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="86c1c-116">Especifica uma tabela de hash que contém pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="86c1c-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="86c1c-117">As chaves representam os campos de conexão do tipo de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="86c1c-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="86c1c-118">Os valores representam os valores específicos de cada campo de conexão para a instância de conexão.</span><span class="sxs-lookup"><span data-stu-id="86c1c-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="86c1c-119">-ConnectionName</span><span class="sxs-lookup"><span data-stu-id="86c1c-119">-ConnectionTypeName</span></span>
<span data-ttu-id="86c1c-120">Especifica o nome do tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="86c1c-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="86c1c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c1c-121">-DefaultProfile</span></span>
<span data-ttu-id="86c1c-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="86c1c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86c1c-123">-Descrição</span><span class="sxs-lookup"><span data-stu-id="86c1c-123">-Description</span></span>
<span data-ttu-id="86c1c-124">Especifica uma descrição para a conexão.</span><span class="sxs-lookup"><span data-stu-id="86c1c-124">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="86c1c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="86c1c-125">-Name</span></span>
<span data-ttu-id="86c1c-126">Especifica um nome para a conexão.</span><span class="sxs-lookup"><span data-stu-id="86c1c-126">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="86c1c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c1c-127">-ResourceGroupName</span></span>
<span data-ttu-id="86c1c-128">Especifica o nome do grupo de recursos para o qual esse cmdlet cria uma conexão.</span><span class="sxs-lookup"><span data-stu-id="86c1c-128">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="86c1c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c1c-129">CommonParameters</span></span>
<span data-ttu-id="86c1c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c1c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c1c-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c1c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c1c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86c1c-132">INPUTS</span></span>

### <span data-ttu-id="86c1c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="86c1c-133">System.String</span></span>

### <span data-ttu-id="86c1c-134">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="86c1c-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="86c1c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86c1c-135">OUTPUTS</span></span>

### <span data-ttu-id="86c1c-136">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="86c1c-136">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="86c1c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86c1c-137">NOTES</span></span>

## <span data-ttu-id="86c1c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86c1c-138">RELATED LINKS</span></span>

[<span data-ttu-id="86c1c-139">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="86c1c-139">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="86c1c-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="86c1c-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


