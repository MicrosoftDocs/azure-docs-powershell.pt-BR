---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 72ad39ef5b63482b10623c1945c0fb5280e07603
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889735"
---
# <span data-ttu-id="09e5d-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="09e5d-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="09e5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="09e5d-103">Define a política de proteção de informações SQL locatário efetivo.</span><span class="sxs-lookup"><span data-stu-id="09e5d-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="09e5d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="09e5d-104">SYNTAX</span></span>

### <span data-ttu-id="09e5d-105">SQL Política de Proteção de Informações (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09e5d-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09e5d-106">SQL caminho do arquivo de política de proteção de informações</span><span class="sxs-lookup"><span data-stu-id="09e5d-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09e5d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="09e5d-107">DESCRIPTION</span></span>
<span data-ttu-id="09e5d-108">Define a política de proteção de informações SQL locatário efetivo.</span><span class="sxs-lookup"><span data-stu-id="09e5d-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="09e5d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09e5d-109">EXAMPLES</span></span>

### <span data-ttu-id="09e5d-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="09e5d-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="09e5d-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="09e5d-111">PARAMETERS</span></span>

### <span data-ttu-id="09e5d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09e5d-112">-AsJob</span></span>
<span data-ttu-id="09e5d-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="09e5d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="09e5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e5d-114">-DefaultProfile</span></span>
<span data-ttu-id="09e5d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09e5d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09e5d-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="09e5d-116">-FilePath</span></span>
<span data-ttu-id="09e5d-117">Especifica um caminho de um arquivo .json que contém SQL de Política de Proteção de Informações.</span><span class="sxs-lookup"><span data-stu-id="09e5d-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="09e5d-118">-Policy</span><span class="sxs-lookup"><span data-stu-id="09e5d-118">-Policy</span></span>
<span data-ttu-id="09e5d-119">Especifica uma definição SQL política de proteção de informações.</span><span class="sxs-lookup"><span data-stu-id="09e5d-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="09e5d-120">Você pode especificar um caminho de um arquivo .json ou uma cadeia de caracteres de formato JSON que define a política.</span><span class="sxs-lookup"><span data-stu-id="09e5d-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="09e5d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09e5d-121">-Confirm</span></span>
<span data-ttu-id="09e5d-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09e5d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09e5d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09e5d-123">-WhatIf</span></span>
<span data-ttu-id="09e5d-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09e5d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09e5d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09e5d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09e5d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e5d-126">CommonParameters</span></span>
<span data-ttu-id="09e5d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e5d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e5d-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09e5d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e5d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09e5d-129">INPUTS</span></span>

### <span data-ttu-id="09e5d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="09e5d-130">System.String</span></span>

## <span data-ttu-id="09e5d-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="09e5d-131">OUTPUTS</span></span>

### <span data-ttu-id="09e5d-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="09e5d-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="09e5d-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="09e5d-133">NOTES</span></span>

## <span data-ttu-id="09e5d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09e5d-134">RELATED LINKS</span></span>
