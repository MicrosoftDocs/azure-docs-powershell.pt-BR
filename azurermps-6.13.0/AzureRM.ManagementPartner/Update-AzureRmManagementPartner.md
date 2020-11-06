---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393054
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Update-AzureRmManagementPartner.md
ms.openlocfilehash: 420353d7a8af1046456138918092ca56d5c6ed96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430881"
---
# <span data-ttu-id="b8992-101">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8992-101">Update-AzureRmManagementPartner</span></span>

## <span data-ttu-id="b8992-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8992-102">SYNOPSIS</span></span>
<span data-ttu-id="b8992-103">Atualiza a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="b8992-103">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8992-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8992-104">SYNTAX</span></span>

```
Update-AzureRmManagementPartner [-PartnerId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8992-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8992-105">DESCRIPTION</span></span>
<span data-ttu-id="b8992-106">Atualiza a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="b8992-106">Updates the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="b8992-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8992-107">EXAMPLES</span></span>

### <span data-ttu-id="b8992-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8992-108">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmManagementPartner -PartnerId 4977985
PartnerId   : 4977985
PartnerName : Test_Test_DPORTest
TenantId    : 1b1121dd-6900-412a-af73-e8d44f81e1c1
ObjectId    : aa67f786-0552-423e-8849-244ed12bf581
State       : Active
```

<span data-ttu-id="b8992-109">Atualize o parceiro de gerenciamento para um novo</span><span class="sxs-lookup"><span data-stu-id="b8992-109">Update the management partner to a new one</span></span>

## <span data-ttu-id="b8992-110">OS</span><span class="sxs-lookup"><span data-stu-id="b8992-110">PARAMETERS</span></span>

### <span data-ttu-id="b8992-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8992-111">-DefaultProfile</span></span>
<span data-ttu-id="b8992-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8992-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8992-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="b8992-113">-PartnerId</span></span>
<span data-ttu-id="b8992-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="b8992-114">The management partner id, it is a 6 digits number</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8992-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8992-115">-Confirm</span></span>
<span data-ttu-id="b8992-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8992-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8992-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8992-117">-WhatIf</span></span>
<span data-ttu-id="b8992-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8992-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8992-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8992-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8992-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8992-120">CommonParameters</span></span>
<span data-ttu-id="b8992-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8992-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8992-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8992-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8992-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8992-123">INPUTS</span></span>

### <span data-ttu-id="b8992-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b8992-124">None</span></span>

## <span data-ttu-id="b8992-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8992-125">OUTPUTS</span></span>

### <span data-ttu-id="b8992-126">Microsoft. Azure. Commands. ManagementPartner. PSManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8992-126">Microsoft.Azure.Commands.ManagementPartner.PSManagementPartner</span></span>

## <span data-ttu-id="b8992-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8992-127">NOTES</span></span>

## <span data-ttu-id="b8992-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8992-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8992-129">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8992-129">Remove-AzureRmManagementPartner</span></span>](./Remove-AzureRmManagementPartner.md)

[<span data-ttu-id="b8992-130">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8992-130">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="b8992-131">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="b8992-131">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)
