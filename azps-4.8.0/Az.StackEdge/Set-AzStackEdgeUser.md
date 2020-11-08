---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeUser.md
ms.openlocfilehash: 707889590efeb17ee676fe3d8b37325bc48fdc81
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113196"
---
# <span data-ttu-id="94bd2-101">Set-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="94bd2-101">Set-AzStackEdgeUser</span></span>

## <span data-ttu-id="94bd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="94bd2-103">Define uma nova senha para um usuário no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="94bd2-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="94bd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94bd2-104">SYNTAX</span></span>

### <span data-ttu-id="94bd2-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="94bd2-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94bd2-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94bd2-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94bd2-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94bd2-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeUser -InputObject <PSStackEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94bd2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94bd2-108">DESCRIPTION</span></span>
<span data-ttu-id="94bd2-109">O cmdlet **set-AzStackEdgeUser** define uma nova senha para um usuário no dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="94bd2-109">The **Set-AzStackEdgeUser** cmdlet sets a new password for a user on the Stack Edge device.</span></span>

## <span data-ttu-id="94bd2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94bd2-110">EXAMPLES</span></span>

### <span data-ttu-id="94bd2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="94bd2-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="94bd2-112">OS</span><span class="sxs-lookup"><span data-stu-id="94bd2-112">PARAMETERS</span></span>

### <span data-ttu-id="94bd2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94bd2-113">-AsJob</span></span>
<span data-ttu-id="94bd2-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="94bd2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94bd2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94bd2-115">-DefaultProfile</span></span>
<span data-ttu-id="94bd2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94bd2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94bd2-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="94bd2-117">-DeviceName</span></span>
<span data-ttu-id="94bd2-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="94bd2-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94bd2-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="94bd2-119">-EncryptionKey</span></span>
<span data-ttu-id="94bd2-120">Chave de criptografia do dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="94bd2-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94bd2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94bd2-121">-InputObject</span></span>
<span data-ttu-id="94bd2-122">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="94bd2-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases: User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94bd2-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="94bd2-123">-Name</span></span>
<span data-ttu-id="94bd2-124">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="94bd2-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94bd2-125">-Senha</span><span class="sxs-lookup"><span data-stu-id="94bd2-125">-Password</span></span>
<span data-ttu-id="94bd2-126">Senha, fornecer como uma cadeia de caracteres segura</span><span class="sxs-lookup"><span data-stu-id="94bd2-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94bd2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94bd2-127">-ResourceGroupName</span></span>
<span data-ttu-id="94bd2-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="94bd2-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94bd2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94bd2-129">-ResourceId</span></span>
<span data-ttu-id="94bd2-130">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="94bd2-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94bd2-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94bd2-131">-Confirm</span></span>
<span data-ttu-id="94bd2-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94bd2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94bd2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94bd2-133">-WhatIf</span></span>
<span data-ttu-id="94bd2-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94bd2-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94bd2-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94bd2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94bd2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94bd2-136">CommonParameters</span></span>
<span data-ttu-id="94bd2-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94bd2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94bd2-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94bd2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94bd2-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94bd2-139">INPUTS</span></span>

### <span data-ttu-id="94bd2-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="94bd2-140">None</span></span>

## <span data-ttu-id="94bd2-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94bd2-141">OUTPUTS</span></span>

### <span data-ttu-id="94bd2-142">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="94bd2-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="94bd2-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94bd2-143">NOTES</span></span>

## <span data-ttu-id="94bd2-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94bd2-144">RELATED LINKS</span></span>
