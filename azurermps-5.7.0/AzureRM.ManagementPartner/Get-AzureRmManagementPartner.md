---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/get-azurermmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Get-AzureRmManagementPartner.md
ms.openlocfilehash: b1fe94533074860a3c95c05d6609bb8ebb446a9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430995"
---
# <span data-ttu-id="216a6-101">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="216a6-101">Get-AzureRmManagementPartner</span></span>

## <span data-ttu-id="216a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="216a6-102">SYNOPSIS</span></span>
<span data-ttu-id="216a6-103">Obtém a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="216a6-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="216a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="216a6-104">SYNTAX</span></span>

```
Get-AzureRmManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="216a6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="216a6-105">DESCRIPTION</span></span>
<span data-ttu-id="216a6-106">Obtém a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="216a6-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span> 

## <span data-ttu-id="216a6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="216a6-107">EXAMPLES</span></span>

### <span data-ttu-id="216a6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="216a6-108">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="216a6-109">Obter a ID do parceiro de gerenciamento atual</span><span class="sxs-lookup"><span data-stu-id="216a6-109">Get the current management partner id</span></span>

### <span data-ttu-id="216a6-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="216a6-110">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="216a6-111">Obter a ID de parceiro de gerenciamento atual usando uma ID de parceiro, se elas não corresponderem, haverá falha</span><span class="sxs-lookup"><span data-stu-id="216a6-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="216a6-112">OS</span><span class="sxs-lookup"><span data-stu-id="216a6-112">PARAMETERS</span></span>

### <span data-ttu-id="216a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="216a6-113">-DefaultProfile</span></span>
<span data-ttu-id="216a6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="216a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="216a6-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="216a6-115">-PartnerId</span></span>
<span data-ttu-id="216a6-116">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="216a6-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="216a6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="216a6-117">CommonParameters</span></span>
<span data-ttu-id="216a6-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="216a6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="216a6-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="216a6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="216a6-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="216a6-120">INPUTS</span></span>

### <span data-ttu-id="216a6-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="216a6-121">None</span></span>

## <span data-ttu-id="216a6-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="216a6-122">OUTPUTS</span></span>

### <span data-ttu-id="216a6-123">Microsoft. Azure. Commands. Resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="216a6-123">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="216a6-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="216a6-124">NOTES</span></span>

## <span data-ttu-id="216a6-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="216a6-125">RELATED LINKS</span></span>

[<span data-ttu-id="216a6-126">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="216a6-126">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="216a6-127">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="216a6-127">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="216a6-128">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="216a6-128">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)