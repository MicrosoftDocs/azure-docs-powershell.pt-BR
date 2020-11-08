---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 3b433860cda56f827bb58bc135240da41b89ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110870"
---
# <span data-ttu-id="b67d2-101">Set-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b67d2-101">Set-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="b67d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b67d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b67d2-103">Define a política de proteção de informações SQL do locatário efetivo.</span><span class="sxs-lookup"><span data-stu-id="b67d2-103">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="b67d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b67d2-104">SYNTAX</span></span>

### <span data-ttu-id="b67d2-105">Política de proteção de informações do SQL (padrão)</span><span class="sxs-lookup"><span data-stu-id="b67d2-105">SQL Information Protection Policy (Default)</span></span>
```
Set-AzSqlInformationProtectionPolicy -Policy <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b67d2-106">Caminho do arquivo de política de proteção de informações SQL</span><span class="sxs-lookup"><span data-stu-id="b67d2-106">SQL Information Protection Policy File Path</span></span>
```
Set-AzSqlInformationProtectionPolicy -FilePath <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b67d2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b67d2-107">DESCRIPTION</span></span>
<span data-ttu-id="b67d2-108">Define a política de proteção de informações SQL do locatário efetivo.</span><span class="sxs-lookup"><span data-stu-id="b67d2-108">Sets the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="b67d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b67d2-109">EXAMPLES</span></span>

### <span data-ttu-id="b67d2-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b67d2-110">Example</span></span>
```powershell
PS C:\> Set-AzSqlInformationProtectionPolicy -FilePath "C:\Users\myUser\Desktop\policy.json"
```

## <span data-ttu-id="b67d2-111">OS</span><span class="sxs-lookup"><span data-stu-id="b67d2-111">PARAMETERS</span></span>

### <span data-ttu-id="b67d2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b67d2-112">-AsJob</span></span>
<span data-ttu-id="b67d2-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b67d2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b67d2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b67d2-114">-DefaultProfile</span></span>
<span data-ttu-id="b67d2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b67d2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b67d2-116">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b67d2-116">-FilePath</span></span>
<span data-ttu-id="b67d2-117">Especifica um caminho de um arquivo. JSON que contém a definição da política de proteção de informações SQL.</span><span class="sxs-lookup"><span data-stu-id="b67d2-117">Specifies a path of a .json file containing SQL Information Protection Policy definition.</span></span>

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

### <span data-ttu-id="b67d2-118">-Política</span><span class="sxs-lookup"><span data-stu-id="b67d2-118">-Policy</span></span>
<span data-ttu-id="b67d2-119">Especifica uma definição de política de proteção de informações do SQL.</span><span class="sxs-lookup"><span data-stu-id="b67d2-119">Specifies a SQL information protection policy definition.</span></span> <span data-ttu-id="b67d2-120">Você pode especificar um caminho de um arquivo. JSON ou uma cadeia de caracteres de formato JSON que define a política.</span><span class="sxs-lookup"><span data-stu-id="b67d2-120">You can specify a path of a .json file or a JSON format string that defines the policy.</span></span>

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

### <span data-ttu-id="b67d2-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b67d2-121">-Confirm</span></span>
<span data-ttu-id="b67d2-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b67d2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b67d2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b67d2-123">-WhatIf</span></span>
<span data-ttu-id="b67d2-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b67d2-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b67d2-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b67d2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b67d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b67d2-126">CommonParameters</span></span>
<span data-ttu-id="b67d2-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b67d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b67d2-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b67d2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b67d2-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b67d2-129">INPUTS</span></span>

### <span data-ttu-id="b67d2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b67d2-130">System.String</span></span>

## <span data-ttu-id="b67d2-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b67d2-131">OUTPUTS</span></span>

### <span data-ttu-id="b67d2-132">Microsoft. Azure. Commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b67d2-132">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="b67d2-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b67d2-133">NOTES</span></span>

## <span data-ttu-id="b67d2-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b67d2-134">RELATED LINKS</span></span>
