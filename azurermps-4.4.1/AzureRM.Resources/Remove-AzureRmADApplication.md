---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 0b0b560a97e223820a3a73ce036a5d7599df9a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432559"
---
# <span data-ttu-id="5829b-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5829b-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="5829b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5829b-102">SYNOPSIS</span></span>
<span data-ttu-id="5829b-103">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5829b-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5829b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5829b-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5829b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5829b-105">DESCRIPTION</span></span>
<span data-ttu-id="5829b-106">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5829b-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="5829b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5829b-107">EXAMPLES</span></span>

### <span data-ttu-id="5829b-108">--------------------------Excluir o aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="5829b-108">--------------------------  Delete AAD application.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="5829b-109">Exclui o aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5829b-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="5829b-110">OS</span><span class="sxs-lookup"><span data-stu-id="5829b-110">PARAMETERS</span></span>

### <span data-ttu-id="5829b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5829b-111">-Force</span></span>
<span data-ttu-id="5829b-112">Alternar para excluir um aplicativo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="5829b-112">Switch to delete an application without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5829b-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5829b-113">-ObjectId</span></span>
<span data-ttu-id="5829b-114">A ID do objeto do aplicativo a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="5829b-114">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5829b-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5829b-115">-Confirm</span></span>
<span data-ttu-id="5829b-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5829b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5829b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5829b-117">-WhatIf</span></span>
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

### <span data-ttu-id="5829b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5829b-118">-DefaultProfile</span></span>
<span data-ttu-id="5829b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5829b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5829b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5829b-120">CommonParameters</span></span>
<span data-ttu-id="5829b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5829b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5829b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5829b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5829b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5829b-123">INPUTS</span></span>

## <span data-ttu-id="5829b-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5829b-124">OUTPUTS</span></span>

## <span data-ttu-id="5829b-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5829b-125">NOTES</span></span>
<span data-ttu-id="5829b-126">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="5829b-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5829b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5829b-127">RELATED LINKS</span></span>

[<span data-ttu-id="5829b-128">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5829b-128">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="5829b-129">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5829b-129">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="5829b-130">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5829b-130">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="5829b-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="5829b-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

