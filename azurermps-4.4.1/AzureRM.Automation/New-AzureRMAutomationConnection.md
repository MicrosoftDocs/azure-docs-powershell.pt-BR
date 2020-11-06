---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 95103160-8101-4C43-8DAA-0BD75DFF3150
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationConnection.md
ms.openlocfilehash: 2964102dbb3f12b797d3d551f7bd4097ca8836a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431182"
---
# <span data-ttu-id="ba0cc-101">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="ba0cc-101">New-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="ba0cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="ba0cc-103">Cria uma conexão de automação.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-103">Creates an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba0cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba0cc-104">SYNTAX</span></span>

```
New-AzureRmAutomationConnection [-Name] <String> [-ConnectionTypeName] <String>
 [-ConnectionFieldValues] <IDictionary> [-Description <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba0cc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="ba0cc-106">O cmdlet **New-AzureRmAutomationConnection** cria uma conexão na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-106">The **New-AzureRmAutomationConnection** cmdlet creates a connection in Azure Automation.</span></span>

## <span data-ttu-id="ba0cc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba0cc-107">EXAMPLES</span></span>

### <span data-ttu-id="ba0cc-108">Exemplo 1: criar uma conexão</span><span class="sxs-lookup"><span data-stu-id="ba0cc-108">Example 1: Create a connection</span></span>
```
PS C:\>$FieldValues = @{"AutomationCertificateName"="ContosoCertificate";"SubscriptionID"="81b59010-dc55-45b7-89cd-5ca26db62472"}
PS C:\> New-AzureRmAutomationConnection -Name "Connection12" -ConnectionTypeName Azure -ConnectionFieldValues $FieldValues -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="ba0cc-109">O primeiro comando atribui uma tabela de hash de valores de campo à variável $FieldValue.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-109">The first command assigns a hash table of field values to the $FieldValue variable.</span></span>

<span data-ttu-id="ba0cc-110">O segundo comando cria uma conexão do Azure chamada Connection12 na conta de automação chamada AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-110">The second command creates an Azure connection named Connection12 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="ba0cc-111">O comando usa os valores do campo de conexão em $FieldValues.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-111">The command uses the connection field values in $FieldValues.</span></span>

## <span data-ttu-id="ba0cc-112">OS</span><span class="sxs-lookup"><span data-stu-id="ba0cc-112">PARAMETERS</span></span>

### <span data-ttu-id="ba0cc-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba0cc-113">-AutomationAccountName</span></span>
<span data-ttu-id="ba0cc-114">Especifica o nome da conta de automação para a qual esse cmdlet cria uma conexão.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-114">Specifies the name of the Automation account for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="ba0cc-115">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="ba0cc-115">-ConnectionFieldValues</span></span>
<span data-ttu-id="ba0cc-116">Especifica uma tabela de hash que contém pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-116">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="ba0cc-117">As chaves representam os campos de conexão do tipo de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-117">The keys represent the connection fields for the specified connection type.</span></span>
<span data-ttu-id="ba0cc-118">Os valores representam os valores específicos de cada campo de conexão para a instância de conexão.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-118">The values represent the specific values of each connection field for the connection instance.</span></span>

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

### <span data-ttu-id="ba0cc-119">-ConnectionName</span><span class="sxs-lookup"><span data-stu-id="ba0cc-119">-ConnectionTypeName</span></span>
<span data-ttu-id="ba0cc-120">Especifica o nome do tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-120">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="ba0cc-121">-Descrição</span><span class="sxs-lookup"><span data-stu-id="ba0cc-121">-Description</span></span>
<span data-ttu-id="ba0cc-122">Especifica uma descrição para a conexão.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-122">Specifies a description for the connection.</span></span>

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

### <span data-ttu-id="ba0cc-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba0cc-123">-Name</span></span>
<span data-ttu-id="ba0cc-124">Especifica um nome para a conexão.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-124">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="ba0cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba0cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="ba0cc-126">Especifica o nome do grupo de recursos para o qual esse cmdlet cria uma conexão.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-126">Specifies the name of the resource group for which this cmdlet creates a connection.</span></span>

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

### <span data-ttu-id="ba0cc-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba0cc-127">-DefaultProfile</span></span>
<span data-ttu-id="ba0cc-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba0cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba0cc-129">CommonParameters</span></span>
<span data-ttu-id="ba0cc-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba0cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba0cc-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba0cc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba0cc-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba0cc-132">INPUTS</span></span>

## <span data-ttu-id="ba0cc-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba0cc-133">OUTPUTS</span></span>

### <span data-ttu-id="ba0cc-134">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="ba0cc-134">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="ba0cc-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba0cc-135">NOTES</span></span>

## <span data-ttu-id="ba0cc-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba0cc-136">RELATED LINKS</span></span>

[<span data-ttu-id="ba0cc-137">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="ba0cc-137">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="ba0cc-138">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="ba0cc-138">Remove-AzureRmAutomationConnection</span></span>](./Remove-AzureRMAutomationConnection.md)


