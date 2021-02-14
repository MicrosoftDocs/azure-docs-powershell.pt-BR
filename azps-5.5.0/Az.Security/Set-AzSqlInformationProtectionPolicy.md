---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117163"
---
# <span data-ttu-id="001f0-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="001f0-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="001f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="001f0-102">SYNOPSIS</span></span>
<span data-ttu-id="001f0-103">Define a política efetiva de proteção de informações SQL do locatário.</span><span class="sxs-lookup"><span data-stu-id="001f0-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="001f0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="001f0-104">SYNTAX</span></span>

### <span data-ttu-id="001f0-105">Política de Proteção de Informações DO SQL (Padrão)</span><span class="sxs-lookup"><span data-stu-id="001f0-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="001f0-106">Caminho do Arquivo de Política de Proteção de Informações do SQL</span><span class="sxs-lookup"><span data-stu-id="001f0-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="001f0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="001f0-107">DESCRIPTION</span></span>
<span data-ttu-id="001f0-108">Define a política efetiva de proteção de informações SQL do locatário.</span><span class="sxs-lookup"><span data-stu-id="001f0-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="001f0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="001f0-109">EXAMPLES</span></span>

### <span data-ttu-id="001f0-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="001f0-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="001f0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="001f0-111">PARAMETERS</span></span>

### <span data-ttu-id="001f0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="001f0-112">-AsJob</span></span>
<span data-ttu-id="001f0-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="001f0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="001f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="001f0-114">-DefaultProfile</span></span>
<span data-ttu-id="001f0-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="001f0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="001f0-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="001f0-116">-FilePath</span></span>
<span data-ttu-id="001f0-117">Especifica um caminho de um arquivo .json que contém a definição da Política de Proteção de Informações sql.</span><span class="sxs-lookup"><span data-stu-id="001f0-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy File Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="001f0-118">-Política</span><span class="sxs-lookup"><span data-stu-id="001f0-118">-Policy</span></span>
<span data-ttu-id="001f0-119">Especifica uma definição de política de proteção de informações SQL.</span><span class="sxs-lookup"><span data-stu-id="001f0-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="001f0-120">Você pode especificar um caminho de um arquivo .json ou uma cadeia de caracteres de formato JSON que define a política.</span><span class="sxs-lookup"><span data-stu-id="001f0-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SQL Information Protection Policy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="001f0-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="001f0-121">-Confirm</span></span>
<span data-ttu-id="001f0-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="001f0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="001f0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="001f0-123">-WhatIf</span></span>
<span data-ttu-id="001f0-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="001f0-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="001f0-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="001f0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="001f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001f0-126">CommonParameters</span></span>
<span data-ttu-id="001f0-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="001f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001f0-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="001f0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001f0-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="001f0-129">INPUTS</span></span>

### <span data-ttu-id="001f0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="001f0-130">System.String</span></span>

## <span data-ttu-id="001f0-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="001f0-131">OUTPUTS</span></span>

### <span data-ttu-id="001f0-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="001f0-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="001f0-133">Notas</span><span class="sxs-lookup"><span data-stu-id="001f0-133">NOTES</span></span>

## <span data-ttu-id="001f0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="001f0-134">RELATED LINKS</span></span>
