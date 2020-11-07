---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946220"
---
# <span data-ttu-id="4c244-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4c244-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="4c244-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c244-102">SYNOPSIS</span></span>

<span data-ttu-id="4c244-103">Cria uma conexão na automação.</span><span class="sxs-lookup"><span data-stu-id="4c244-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="4c244-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c244-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4c244-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c244-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4c244-106">O cmdlet **New-AzureAutomationConnection** cria uma conexão na automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4c244-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="4c244-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c244-107">EXAMPLES</span></span>

## <span data-ttu-id="4c244-108">OS</span><span class="sxs-lookup"><span data-stu-id="4c244-108">PARAMETERS</span></span>

### <span data-ttu-id="4c244-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4c244-109">-AutomationAccountName</span></span>
<span data-ttu-id="4c244-110">Especifica o nome da conta de automação na qual a conexão será armazenada.</span><span class="sxs-lookup"><span data-stu-id="4c244-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c244-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="4c244-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="4c244-112">Especifica uma tabela de hash que contém pares de chave/valor.</span><span class="sxs-lookup"><span data-stu-id="4c244-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="4c244-113">As chaves representam os campos de conexão no tipo de conexão especificado.</span><span class="sxs-lookup"><span data-stu-id="4c244-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="4c244-114">Os valores representam os valores específicos para armazenar para cada campo de conexão para a instância de conexão.</span><span class="sxs-lookup"><span data-stu-id="4c244-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c244-115">-ConnectionName</span><span class="sxs-lookup"><span data-stu-id="4c244-115">-ConnectionTypeName</span></span>
<span data-ttu-id="4c244-116">Especifica o nome do tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="4c244-116">Specifies the name of the connection type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c244-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="4c244-117">-Description</span></span>
<span data-ttu-id="4c244-118">Especifica uma descrição para a credencial.</span><span class="sxs-lookup"><span data-stu-id="4c244-118">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="4c244-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c244-119">-Name</span></span>
<span data-ttu-id="4c244-120">Especifica um nome para a conexão.</span><span class="sxs-lookup"><span data-stu-id="4c244-120">Specifies a name for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c244-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4c244-121">-Profile</span></span>
<span data-ttu-id="4c244-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4c244-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c244-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4c244-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c244-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c244-124">CommonParameters</span></span>
<span data-ttu-id="4c244-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c244-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c244-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c244-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c244-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c244-127">INPUTS</span></span>

## <span data-ttu-id="4c244-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c244-128">OUTPUTS</span></span>

### <span data-ttu-id="4c244-129">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="4c244-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="4c244-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c244-130">NOTES</span></span>

## <span data-ttu-id="4c244-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c244-131">RELATED LINKS</span></span>

[<span data-ttu-id="4c244-132">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4c244-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="4c244-133">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="4c244-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="4c244-134">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="4c244-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


