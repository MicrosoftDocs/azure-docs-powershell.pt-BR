---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: DBA7AD5F-CC13-417A-B753-F998942530BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagement.md
ms.openlocfilehash: 610f8589dbb6c01cae1a3eb37f886425a3664929
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427048"
---
# <span data-ttu-id="f086b-101">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f086b-101">Get-AzureRmApiManagement</span></span>

## <span data-ttu-id="f086b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f086b-102">SYNOPSIS</span></span>
<span data-ttu-id="f086b-103">Obtém uma lista ou uma descrição de serviço de gerenciamento de API específica.</span><span class="sxs-lookup"><span data-stu-id="f086b-103">Gets a list or a particular API Management Service description.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f086b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f086b-104">SYNTAX</span></span>

### <span data-ttu-id="f086b-105">Todos na assinatura (padrão)</span><span class="sxs-lookup"><span data-stu-id="f086b-105">All In Subscription (Default)</span></span>
```
Get-AzureRmApiManagement [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f086b-106">Tudo no grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f086b-106">All In Resource Group</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f086b-107">Serviço de gerenciamento de API específico</span><span class="sxs-lookup"><span data-stu-id="f086b-107">Specific API Management Service</span></span>
```
Get-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f086b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f086b-108">DESCRIPTION</span></span>
<span data-ttu-id="f086b-109">O cmdlet **Get-AzureRmApiManagement** Obtém uma lista de todos os serviços de gerenciamento de API sob assinatura ou grupo de recursos especificado ou um gerenciamento de API específico.</span><span class="sxs-lookup"><span data-stu-id="f086b-109">The **Get-AzureRmApiManagement** cmdlet gets a list of all API Management services under subscription or specified resource group or a particular API Management.</span></span>

## <span data-ttu-id="f086b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f086b-110">EXAMPLES</span></span>

### <span data-ttu-id="f086b-111">Exemplo 1: obter todos os serviços de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="f086b-111">Example 1: Get all API Management services</span></span>
```
PS C:\>Get-AzureRmApiManagement
```

<span data-ttu-id="f086b-112">Esse comando obtém todos os serviços de gerenciamento de API em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f086b-112">This command gets all API Management services within a subscription.</span></span>

### <span data-ttu-id="f086b-113">Exemplo 2: obter todos os serviços de gerenciamento de API por um nome específico</span><span class="sxs-lookup"><span data-stu-id="f086b-113">Example 2: Get all API Management services by a specific name</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
```

<span data-ttu-id="f086b-114">Esse comando obtém todo o serviço de gerenciamento de API por nome.</span><span class="sxs-lookup"><span data-stu-id="f086b-114">This command gets all API Management service by name.</span></span>

## <span data-ttu-id="f086b-115">OS</span><span class="sxs-lookup"><span data-stu-id="f086b-115">PARAMETERS</span></span>

### <span data-ttu-id="f086b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f086b-116">-Name</span></span>
<span data-ttu-id="f086b-117">Especifica o nome do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f086b-117">Specifies the name of API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f086b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f086b-118">-ResourceGroupName</span></span>
<span data-ttu-id="f086b-119">Especifica o nome do grupo de recursos em que esse cmdlet obtém o serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="f086b-119">Specifies the name of the resource group under in which this cmdlet gets the API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific API Management Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f086b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f086b-120">-DefaultProfile</span></span>
<span data-ttu-id="f086b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f086b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f086b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f086b-122">CommonParameters</span></span>
<span data-ttu-id="f086b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f086b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f086b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f086b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f086b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f086b-125">INPUTS</span></span>

## <span data-ttu-id="f086b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f086b-126">OUTPUTS</span></span>

### <span data-ttu-id="f086b-127">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement]</span><span class="sxs-lookup"><span data-stu-id="f086b-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement]</span></span>

## <span data-ttu-id="f086b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f086b-128">NOTES</span></span>

## <span data-ttu-id="f086b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f086b-129">RELATED LINKS</span></span>

[<span data-ttu-id="f086b-130">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f086b-130">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="f086b-131">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f086b-131">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="f086b-132">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f086b-132">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="f086b-133">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="f086b-133">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


