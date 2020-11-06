---
external help file: Microsoft.Azure.Commands.ManagementPartner.dll-Help.xml
Module Name: AzureRM.ManagementPartner
online version: https://go.microsoft.com/fwlink/?LinkID=393045
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagementPartner/Commands.Partner/help/Remove-AzureRmManagementPartner.md
ms.openlocfilehash: 703c38d02ef6a6a339c58c861961cd2ad92ecb7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432114"
---
# <span data-ttu-id="3ae13-101">Remove-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3ae13-101">Remove-AzureRmManagementPartner</span></span>

## <span data-ttu-id="3ae13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ae13-102">SYNOPSIS</span></span>
<span data-ttu-id="3ae13-103">Exclua a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="3ae13-103">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ae13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ae13-104">SYNTAX</span></span>

```
Remove-AzureRmManagementPartner [-PartnerId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ae13-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ae13-105">DESCRIPTION</span></span>
<span data-ttu-id="3ae13-106">Exclua a ID da MPN (Microsoft Partner Network) do usuário ou entidade de serviço atual autenticado.</span><span class="sxs-lookup"><span data-stu-id="3ae13-106">Delete the Microsoft Partner Network(MPN) ID of the current authenticated user or service principal.</span></span>

## <span data-ttu-id="3ae13-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ae13-107">EXAMPLES</span></span>

### <span data-ttu-id="3ae13-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3ae13-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzureRmManagementPartner -PartnerId 123457 -PassThru
true
```

<span data-ttu-id="3ae13-109">Remover parceiro de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="3ae13-109">Remove management partner</span></span> 

## <span data-ttu-id="3ae13-110">OS</span><span class="sxs-lookup"><span data-stu-id="3ae13-110">PARAMETERS</span></span>

### <span data-ttu-id="3ae13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ae13-111">-DefaultProfile</span></span>
<span data-ttu-id="3ae13-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ae13-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ae13-113">-PartnerId</span><span class="sxs-lookup"><span data-stu-id="3ae13-113">-PartnerId</span></span>
<span data-ttu-id="3ae13-114">A ID do parceiro de gerenciamento, é um número de 6 dígitos</span><span class="sxs-lookup"><span data-stu-id="3ae13-114">The management partner id, it is a 6 digits number</span></span>

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

### <span data-ttu-id="3ae13-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ae13-115">-PassThru</span></span>
<span data-ttu-id="3ae13-116">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="3ae13-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ae13-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ae13-117">-Confirm</span></span>
<span data-ttu-id="3ae13-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ae13-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ae13-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ae13-119">-WhatIf</span></span>
<span data-ttu-id="3ae13-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ae13-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ae13-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ae13-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ae13-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ae13-122">CommonParameters</span></span>
<span data-ttu-id="3ae13-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ae13-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ae13-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ae13-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ae13-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ae13-125">INPUTS</span></span>

### <span data-ttu-id="3ae13-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3ae13-126">None</span></span>

## <span data-ttu-id="3ae13-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ae13-127">OUTPUTS</span></span>

### <span data-ttu-id="3ae13-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="3ae13-128">System.Object</span></span>

## <span data-ttu-id="3ae13-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ae13-129">NOTES</span></span>

## <span data-ttu-id="3ae13-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ae13-130">RELATED LINKS</span></span>

[<span data-ttu-id="3ae13-131">New-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3ae13-131">New-AzureRmManagementPartner</span></span>](./New-AzureRmManagementPartner.md)

[<span data-ttu-id="3ae13-132">Get-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3ae13-132">Get-AzureRmManagementPartner</span></span>](./Get-AzureRmManagementPartner.md)

[<span data-ttu-id="3ae13-133">Update-AzureRmManagementPartner</span><span class="sxs-lookup"><span data-stu-id="3ae13-133">Update-AzureRmManagementPartner</span></span>](./Update-AzureRmManagementPartner.md)