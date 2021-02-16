---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116398"
---
# <span data-ttu-id="a7768-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7768-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="a7768-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7768-102">SYNOPSIS</span></span>
<span data-ttu-id="a7768-103">Recupera a política efetiva de proteção de informações SQL do locatário.</span><span class="sxs-lookup"><span data-stu-id="a7768-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="a7768-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7768-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7768-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7768-105">DESCRIPTION</span></span>
<span data-ttu-id="a7768-106">Recupera a política efetiva de proteção de informações SQL do locatário.</span><span class="sxs-lookup"><span data-stu-id="a7768-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="a7768-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a7768-107">EXAMPLES</span></span>

### <span data-ttu-id="a7768-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a7768-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="a7768-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7768-109">PARAMETERS</span></span>

### <span data-ttu-id="a7768-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7768-110">-AsJob</span></span>
<span data-ttu-id="a7768-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a7768-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7768-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7768-112">-DefaultProfile</span></span>
<span data-ttu-id="a7768-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7768-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7768-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7768-114">CommonParameters</span></span>
<span data-ttu-id="a7768-115">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7768-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7768-116">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7768-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7768-117">Entradas</span><span class="sxs-lookup"><span data-stu-id="a7768-117">INPUTS</span></span>

### <span data-ttu-id="a7768-118">System.string</span><span class="sxs-lookup"><span data-stu-id="a7768-118">System.string</span></span>

## <span data-ttu-id="a7768-119">Saídas</span><span class="sxs-lookup"><span data-stu-id="a7768-119">OUTPUTS</span></span>

### <span data-ttu-id="a7768-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a7768-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="a7768-121">Notas</span><span class="sxs-lookup"><span data-stu-id="a7768-121">NOTES</span></span>

## <span data-ttu-id="a7768-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7768-122">RELATED LINKS</span></span>
