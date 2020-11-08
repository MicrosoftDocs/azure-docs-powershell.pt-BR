---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116197"
---
# <span data-ttu-id="7dd26-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7dd26-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="7dd26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7dd26-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd26-103">Recupera a política de proteção de informações SQL do locatário efetivo.</span><span class="sxs-lookup"><span data-stu-id="7dd26-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="7dd26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7dd26-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dd26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7dd26-105">DESCRIPTION</span></span>
<span data-ttu-id="7dd26-106">Recupera a política de proteção de informações SQL do locatário efetivo.</span><span class="sxs-lookup"><span data-stu-id="7dd26-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="7dd26-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7dd26-107">EXAMPLES</span></span>

### <span data-ttu-id="7dd26-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7dd26-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="7dd26-109">OS</span><span class="sxs-lookup"><span data-stu-id="7dd26-109">PARAMETERS</span></span>

### <span data-ttu-id="7dd26-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7dd26-110">-AsJob</span></span>
<span data-ttu-id="7dd26-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7dd26-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7dd26-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd26-112">-DefaultProfile</span></span>
<span data-ttu-id="7dd26-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7dd26-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dd26-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd26-114">CommonParameters</span></span>
<span data-ttu-id="7dd26-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dd26-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd26-116">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7dd26-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd26-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7dd26-117">INPUTS</span></span>

### <span data-ttu-id="7dd26-118">System. String</span><span class="sxs-lookup"><span data-stu-id="7dd26-118">System.string</span></span>

## <span data-ttu-id="7dd26-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7dd26-119">OUTPUTS</span></span>

### <span data-ttu-id="7dd26-120">Microsoft. Azure. Commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7dd26-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="7dd26-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7dd26-121">NOTES</span></span>

## <span data-ttu-id="7dd26-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7dd26-122">RELATED LINKS</span></span>
