---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946370"
---
# <span data-ttu-id="c0af9-101">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c0af9-101">Get-AzureAutomationConnection</span></span>

## <span data-ttu-id="c0af9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0af9-102">SYNOPSIS</span></span>

<span data-ttu-id="c0af9-103">Obtém uma conexão de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0af9-103">Gets an Azure Automation connection.</span></span>

## <span data-ttu-id="c0af9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0af9-104">SYNTAX</span></span>

### <span data-ttu-id="c0af9-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0af9-105">ByAll (Default)</span></span>
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c0af9-106">ByConnectionName</span><span class="sxs-lookup"><span data-stu-id="c0af9-106">ByConnectionName</span></span>
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0af9-107">ByConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="c0af9-107">ByConnectionTypeName</span></span>
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c0af9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0af9-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="c0af9-109">O cmdlet **Get-AzureAutomationConnection** Obtém uma ou mais conexões de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c0af9-109">The **Get-AzureAutomationConnection** cmdlet gets one or more Microsoft Azure Automation connections.</span></span>
<span data-ttu-id="c0af9-110">Por padrão, todas as conexões são retornadas.</span><span class="sxs-lookup"><span data-stu-id="c0af9-110">By default, all connections are returned.</span></span>
<span data-ttu-id="c0af9-111">Para obter uma conexão específica, especifique o nome dela.</span><span class="sxs-lookup"><span data-stu-id="c0af9-111">To get a specific connection, specify its name.</span></span>
<span data-ttu-id="c0af9-112">Para obter todas as conexões de um determinado tipo, especifique o nome do tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="c0af9-112">To get all connections of a certain type, specify the connection type name.</span></span>

## <span data-ttu-id="c0af9-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0af9-113">EXAMPLES</span></span>

### <span data-ttu-id="c0af9-114">Exemplo 1: obter todas as conexões</span><span class="sxs-lookup"><span data-stu-id="c0af9-114">Example 1: Get all connections</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c0af9-115">Esse comando obtém todas as conexões na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c0af9-115">This command gets all connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c0af9-116">Exemplo 2: obter todas as conexões de um tipo</span><span class="sxs-lookup"><span data-stu-id="c0af9-116">Example 2: Get all connections of a type</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

<span data-ttu-id="c0af9-117">Esse comando obtém todas as conexões do Azure na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c0af9-117">This command gets all Azure connections in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c0af9-118">Exemplo 3: obter uma conexão</span><span class="sxs-lookup"><span data-stu-id="c0af9-118">Example 3: Get a connection</span></span>
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

<span data-ttu-id="c0af9-119">Esse comando obtém a conexão chamada myconnecting.</span><span class="sxs-lookup"><span data-stu-id="c0af9-119">This command gets the connection named MyConnection.</span></span>

## <span data-ttu-id="c0af9-120">OS</span><span class="sxs-lookup"><span data-stu-id="c0af9-120">PARAMETERS</span></span>

### <span data-ttu-id="c0af9-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0af9-121">-AutomationAccountName</span></span>
<span data-ttu-id="c0af9-122">Especifica o nome da conta de automação com a conexão a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="c0af9-122">Specifies the name of the automation account with the connection to retrieve.</span></span>

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

### <span data-ttu-id="c0af9-123">-ConnectionName</span><span class="sxs-lookup"><span data-stu-id="c0af9-123">-ConnectionTypeName</span></span>
<span data-ttu-id="c0af9-124">Especifica o nome de um tipo de conexão para as conexões a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="c0af9-124">Specifies the name of a connection type for the connections to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0af9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0af9-125">-Name</span></span>
<span data-ttu-id="c0af9-126">Especifica o nome de uma conexão a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="c0af9-126">Specifies the name of a connection to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0af9-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c0af9-127">-Profile</span></span>
<span data-ttu-id="c0af9-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c0af9-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c0af9-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c0af9-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c0af9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0af9-130">CommonParameters</span></span>
<span data-ttu-id="c0af9-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0af9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0af9-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0af9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0af9-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0af9-133">INPUTS</span></span>

## <span data-ttu-id="c0af9-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0af9-134">OUTPUTS</span></span>

### <span data-ttu-id="c0af9-135">Microsoft. Azure. Commands. Automation. Model. Connection</span><span class="sxs-lookup"><span data-stu-id="c0af9-135">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="c0af9-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0af9-136">NOTES</span></span>

## <span data-ttu-id="c0af9-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0af9-137">RELATED LINKS</span></span>

[<span data-ttu-id="c0af9-138">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c0af9-138">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="c0af9-139">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="c0af9-139">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="c0af9-140">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="c0af9-140">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


