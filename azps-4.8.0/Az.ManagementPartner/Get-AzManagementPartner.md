---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/en-us/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: 1031c9c8828969d16097953aa7440e2c8c0a8c1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955502"
---
# <span data-ttu-id="b1498-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b1498-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="b1498-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1498-102">SYNOPSIS</span></span>
<span data-ttu-id="b1498-103">Obtém a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="b1498-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b1498-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1498-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1498-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1498-105">DESCRIPTION</span></span>
<span data-ttu-id="b1498-106">Obtém a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="b1498-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b1498-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1498-107">EXAMPLES</span></span>

### <span data-ttu-id="b1498-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1498-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="b1498-109">Obter a ID do parceiro de gerenciamento atual</span><span class="sxs-lookup"><span data-stu-id="b1498-109">Get the current management partner id</span></span>

### <span data-ttu-id="b1498-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b1498-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="b1498-111">Obter a ID de parceiro de gerenciamento atual usando uma ID de parceiro, se elas não corresponderem, haverá falha</span><span class="sxs-lookup"><span data-stu-id="b1498-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="b1498-112">OS</span><span class="sxs-lookup"><span data-stu-id="b1498-112">PARAMETERS</span></span>

### <span data-ttu-id="b1498-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1498-113">-DefaultProfile</span></span>
<span data-ttu-id="b1498-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1498-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1498-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="b1498-115">-PartnerId</span></span>
<span data-ttu-id="b1498-116">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="b1498-116">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1498-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1498-117">CommonParameters</span></span>
<span data-ttu-id="b1498-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1498-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1498-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1498-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1498-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1498-120">INPUTS</span></span>

### <span data-ttu-id="b1498-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b1498-121">None</span></span>

## <span data-ttu-id="b1498-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1498-122">OUTPUTS</span></span>

### <span data-ttu-id="b1498-123">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b1498-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="b1498-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1498-124">NOTES</span></span>

## <span data-ttu-id="b1498-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1498-125">RELATED LINKS</span></span>

[<span data-ttu-id="b1498-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b1498-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="b1498-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b1498-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="b1498-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b1498-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)