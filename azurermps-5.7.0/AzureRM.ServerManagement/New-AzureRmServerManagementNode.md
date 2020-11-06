---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: 498be36141d1a44d33cdcb351b92d5b6908071c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426604"
---
# <span data-ttu-id="ef417-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="ef417-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="ef417-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef417-102">SYNOPSIS</span></span>
<span data-ttu-id="ef417-103">Cria um nó de gerenciamento de servidor.</span><span class="sxs-lookup"><span data-stu-id="ef417-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef417-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef417-104">SYNTAX</span></span>

### <span data-ttu-id="ef417-105">ByName</span><span class="sxs-lookup"><span data-stu-id="ef417-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef417-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="ef417-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef417-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef417-107">DESCRIPTION</span></span>
<span data-ttu-id="ef417-108">O cmdlet **New-AzureRmServerManagementNode** cria um nó de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef417-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="ef417-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef417-109">EXAMPLES</span></span>

## <span data-ttu-id="ef417-110">OS</span><span class="sxs-lookup"><span data-stu-id="ef417-110">PARAMETERS</span></span>

### <span data-ttu-id="ef417-111">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ef417-111">-ComputerName</span></span>
<span data-ttu-id="ef417-112">Especifica o nome do computador que está sendo gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ef417-112">Specifies the computer name of the computer that is being managed.</span></span>

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

### <span data-ttu-id="ef417-113">-Credential</span><span class="sxs-lookup"><span data-stu-id="ef417-113">-Credential</span></span>
<span data-ttu-id="ef417-114">Especifica um objeto **PSCredential** para a conexão com o nó Gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="ef417-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="ef417-115">Para obter um objeto de credencial, use o cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="ef417-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="ef417-116">Para obter mais informações, digite `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ef417-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef417-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef417-117">-DefaultProfile</span></span>
<span data-ttu-id="ef417-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef417-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef417-119">-Gateway</span><span class="sxs-lookup"><span data-stu-id="ef417-119">-Gateway</span></span>
<span data-ttu-id="ef417-120">Especifica o gateway que gerencia o nó.</span><span class="sxs-lookup"><span data-stu-id="ef417-120">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="ef417-121">Esse parâmetro pode ser usado em vez dos parâmetros *ResourceGroupName* , *GATEWAYNAME* e *Location* .</span><span class="sxs-lookup"><span data-stu-id="ef417-121">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef417-122">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="ef417-122">-GatewayName</span></span>
<span data-ttu-id="ef417-123">Especifica o nome do gateway que acessa o nó.</span><span class="sxs-lookup"><span data-stu-id="ef417-123">Specifies the name of the gateway that accesses the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef417-124">-Local</span><span class="sxs-lookup"><span data-stu-id="ef417-124">-Location</span></span>
<span data-ttu-id="ef417-125">Especifica o local em que esse cmdlet cria o nó.</span><span class="sxs-lookup"><span data-stu-id="ef417-125">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef417-126">-NodeName</span><span class="sxs-lookup"><span data-stu-id="ef417-126">-NodeName</span></span>
<span data-ttu-id="ef417-127">Especifica o nome do nó.</span><span class="sxs-lookup"><span data-stu-id="ef417-127">Specifies the name of the node.</span></span>

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

### <span data-ttu-id="ef417-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef417-128">-ResourceGroupName</span></span>
<span data-ttu-id="ef417-129">Especifica o nome do grupo de recursos no qual esse cmdlet cria o nó.</span><span class="sxs-lookup"><span data-stu-id="ef417-129">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef417-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="ef417-130">-Tag</span></span>
<span data-ttu-id="ef417-131">Pares de chave/valor associados ao objeto.</span><span class="sxs-lookup"><span data-stu-id="ef417-131">Key/value pairs associated with the object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef417-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef417-132">CommonParameters</span></span>
<span data-ttu-id="ef417-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef417-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef417-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef417-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef417-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef417-135">INPUTS</span></span>

### <span data-ttu-id="ef417-136">Gateway</span><span class="sxs-lookup"><span data-stu-id="ef417-136">Gateway</span></span>
<span data-ttu-id="ef417-137">O parâmetro ' gateway ' aceita o valor do tipo ' gateway ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="ef417-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="ef417-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef417-138">OUTPUTS</span></span>

### <span data-ttu-id="ef417-139">Microsoft. Azure. Commands. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="ef417-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="ef417-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef417-140">NOTES</span></span>

## <span data-ttu-id="ef417-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef417-141">RELATED LINKS</span></span>

[<span data-ttu-id="ef417-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="ef417-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="ef417-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="ef417-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


