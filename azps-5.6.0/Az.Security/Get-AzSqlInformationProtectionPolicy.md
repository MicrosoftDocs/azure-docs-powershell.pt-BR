---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: da881ceac74810b05385b26f54b7c498c60c2e77
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889884"
---
# <span data-ttu-id="55a24-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="55a24-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="55a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a24-102">SYNOPSIS</span></span>
<span data-ttu-id="55a24-103">Recupera a política de proteção de SQL de informações efetiva.</span><span class="sxs-lookup"><span data-stu-id="55a24-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="55a24-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="55a24-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55a24-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="55a24-105">DESCRIPTION</span></span>
<span data-ttu-id="55a24-106">Recupera a política de proteção de SQL de informações efetiva.</span><span class="sxs-lookup"><span data-stu-id="55a24-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="55a24-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55a24-107">EXAMPLES</span></span>

### <span data-ttu-id="55a24-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="55a24-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="55a24-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="55a24-109">PARAMETERS</span></span>

### <span data-ttu-id="55a24-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55a24-110">-AsJob</span></span>
<span data-ttu-id="55a24-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="55a24-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55a24-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a24-112">-DefaultProfile</span></span>
<span data-ttu-id="55a24-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55a24-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55a24-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a24-114">CommonParameters</span></span>
<span data-ttu-id="55a24-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55a24-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a24-116">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55a24-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a24-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55a24-117">INPUTS</span></span>

### <span data-ttu-id="55a24-118">System.string</span><span class="sxs-lookup"><span data-stu-id="55a24-118">System.string</span></span>

## <span data-ttu-id="55a24-119">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="55a24-119">OUTPUTS</span></span>

### <span data-ttu-id="55a24-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="55a24-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="55a24-121">NOTES</span><span class="sxs-lookup"><span data-stu-id="55a24-121">NOTES</span></span>

## <span data-ttu-id="55a24-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55a24-122">RELATED LINKS</span></span>
