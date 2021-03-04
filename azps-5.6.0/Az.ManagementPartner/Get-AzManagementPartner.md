---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagementPartner.dll-Help.xml
Module Name: Az.ManagementPartner
online version: https://docs.microsoft.com/powershell/module/az.managementpartner/get-azmanagementpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagementPartner/ManagementPartner/help/Get-AzManagementPartner.md
ms.openlocfilehash: e09e63ed68ac87156fd03f73c992043b8a0271cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889271"
---
# <span data-ttu-id="e202e-101">Get-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e202e-101">Get-AzManagementPartner</span></span>

## <span data-ttu-id="e202e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e202e-102">SYNOPSIS</span></span>
<span data-ttu-id="e202e-103">Obtém a ID do MPN (Microsoft Partner Network) do usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="e202e-103">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="e202e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e202e-104">SYNTAX</span></span>

```
Get-AzManagementPartner [[-PartnerId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e202e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e202e-105">DESCRIPTION</span></span>
<span data-ttu-id="e202e-106">Obtém a ID do MPN (Microsoft Partner Network) do usuário ou entidade de serviço autenticado atual.</span><span class="sxs-lookup"><span data-stu-id="e202e-106">Gets the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="e202e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e202e-107">EXAMPLES</span></span>

### <span data-ttu-id="e202e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e202e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzManagementPartner
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="e202e-109">Obter a ID do parceiro de gerenciamento atual</span><span class="sxs-lookup"><span data-stu-id="e202e-109">Get the current management partner id</span></span>

### <span data-ttu-id="e202e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e202e-110">Example 2</span></span>
```powershell
PS C:\> Get-AzManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="e202e-111">Obter a ID do parceiro de gerenciamento atual usando uma id de parceiro, se eles não corresponderem, ele falhará</span><span class="sxs-lookup"><span data-stu-id="e202e-111">Get the current management partner id using a partner id, if they don't match, it will fail</span></span>

## <span data-ttu-id="e202e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e202e-112">PARAMETERS</span></span>

### <span data-ttu-id="e202e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e202e-113">-DefaultProfile</span></span>
<span data-ttu-id="e202e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e202e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e202e-115">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="e202e-115">-PartnerId</span></span>
<span data-ttu-id="e202e-116">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="e202e-116">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="e202e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e202e-117">CommonParameters</span></span>
<span data-ttu-id="e202e-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e202e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e202e-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e202e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e202e-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e202e-120">INPUTS</span></span>

### <span data-ttu-id="e202e-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e202e-121">None</span></span>

## <span data-ttu-id="e202e-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e202e-122">OUTPUTS</span></span>

### <span data-ttu-id="e202e-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e202e-123">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="e202e-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="e202e-124">NOTES</span></span>

## <span data-ttu-id="e202e-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e202e-125">RELATED LINKS</span></span>

[<span data-ttu-id="e202e-126">Remove-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e202e-126">Remove-AzManagementPartner</span></span>](./Remove-AzManagementPartner.md)

[<span data-ttu-id="e202e-127">New-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e202e-127">New-AzManagementPartner</span></span>](./New-AzManagementPartner.md)

[<span data-ttu-id="e202e-128">Update-AzManagementPartner</span><span class="sxs-lookup"><span data-stu-id="e202e-128">Update-AzManagementPartner</span></span>](./Update-AzManagementPartner.md)