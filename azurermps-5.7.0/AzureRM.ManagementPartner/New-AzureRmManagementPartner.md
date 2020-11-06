---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393044
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/New-AzureRmManagementPartner.md
ms.openlocfilehash: 9a6d6d0d21a38ac5ff41460021287e0701de6057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432470"
---
# <span data-ttu-id="19195-101">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="19195-101">New-AzureRmManagementPartner</span></span>

## <span data-ttu-id="19195-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19195-102">SYNOPSIS</span></span>
<span data-ttu-id="19195-103">Associa uma ID do Microsoft Partner Network (MPN) ao usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="19195-103">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19195-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19195-104">SYNTAX</span></span>

```
New-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19195-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19195-105">DESCRIPTION</span></span>
<span data-ttu-id="19195-106">Associa uma ID do Microsoft Partner Network (MPN) ao usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="19195-106">Associates a Microsoft Partner Network(MPN) ID to the current authenticated user or service principal.</span></span>

## <span data-ttu-id="19195-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19195-107">EXAMPLES</span></span>

### <span data-ttu-id="19195-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="19195-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="19195-109">Adicionar um parceiro de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="19195-109">Add a management partner</span></span> 

## <span data-ttu-id="19195-110">OS</span><span class="sxs-lookup"><span data-stu-id="19195-110">PARAMETERS</span></span>

### <span data-ttu-id="19195-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19195-111">-DefaultProfile</span></span>
<span data-ttu-id="19195-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19195-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19195-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="19195-113">-PartnerId</span></span>
<span data-ttu-id="19195-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="19195-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19195-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="19195-115">-Confirm</span></span>
<span data-ttu-id="19195-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19195-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19195-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19195-117">-WhatIf</span></span>
<span data-ttu-id="19195-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="19195-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19195-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="19195-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19195-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19195-120">CommonParameters</span></span>
<span data-ttu-id="19195-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19195-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19195-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19195-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19195-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19195-123">INPUTS</span></span>

### <span data-ttu-id="19195-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="19195-124">None</span></span>

## <span data-ttu-id="19195-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19195-125">OUTPUTS</span></span>

### <span data-ttu-id="19195-126">Microsoft. Azure. Commands. Resources. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="19195-126">Microsoft.Azure.Commands.Resources.PSManagementPartner</span></span>

## <span data-ttu-id="19195-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19195-127">NOTES</span></span>

## <span data-ttu-id="19195-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19195-128">RELATED LINKS</span></span>

[<span data-ttu-id="19195-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="19195-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="19195-130">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="19195-130">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="19195-131">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="19195-131">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)
